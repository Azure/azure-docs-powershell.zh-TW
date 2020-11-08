---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139868"
---
# <span data-ttu-id="77f41-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="77f41-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="77f41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77f41-102">SYNOPSIS</span></span>
<span data-ttu-id="77f41-103">在訂閱或資源群組中取得預算清單。</span><span class="sxs-lookup"><span data-stu-id="77f41-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="77f41-104">句法</span><span class="sxs-lookup"><span data-stu-id="77f41-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="77f41-105">說明</span><span class="sxs-lookup"><span data-stu-id="77f41-105">DESCRIPTION</span></span>
<span data-ttu-id="77f41-106">Get-AzConsumptionBudget Cmdlet 會在訂閱或資源群組中取得預算清單。</span><span class="sxs-lookup"><span data-stu-id="77f41-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="77f41-107">示例</span><span class="sxs-lookup"><span data-stu-id="77f41-107">EXAMPLES</span></span>

### <span data-ttu-id="77f41-108">範例1：取得訂閱層級的預算清單</span><span class="sxs-lookup"><span data-stu-id="77f41-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="77f41-109">範例2：取得資源群組層級的預算清單</span><span class="sxs-lookup"><span data-stu-id="77f41-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="77f41-110">範例3：在訂閱層級使用預算名稱取得預算</span><span class="sxs-lookup"><span data-stu-id="77f41-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="77f41-111">範例4：使用資源群組層級的預算名稱取得預算</span><span class="sxs-lookup"><span data-stu-id="77f41-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="77f41-112">參數</span><span class="sxs-lookup"><span data-stu-id="77f41-112">PARAMETERS</span></span>

### <span data-ttu-id="77f41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f41-113">-DefaultProfile</span></span>
<span data-ttu-id="77f41-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77f41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f41-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="77f41-115">-Name</span></span>
<span data-ttu-id="77f41-116">預算的名稱。</span><span class="sxs-lookup"><span data-stu-id="77f41-116">Name of a budget.</span></span>

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

### <span data-ttu-id="77f41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f41-117">-ResourceGroupName</span></span>
<span data-ttu-id="77f41-118">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="77f41-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="77f41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f41-119">CommonParameters</span></span>
<span data-ttu-id="77f41-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77f41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f41-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77f41-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f41-122">輸入</span><span class="sxs-lookup"><span data-stu-id="77f41-122">INPUTS</span></span>

### <span data-ttu-id="77f41-123">所有</span><span class="sxs-lookup"><span data-stu-id="77f41-123">None</span></span>

## <span data-ttu-id="77f41-124">輸出</span><span class="sxs-lookup"><span data-stu-id="77f41-124">OUTPUTS</span></span>

### <span data-ttu-id="77f41-125">PSBudget 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="77f41-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="77f41-126">筆記</span><span class="sxs-lookup"><span data-stu-id="77f41-126">NOTES</span></span>

## <span data-ttu-id="77f41-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="77f41-127">RELATED LINKS</span></span>
