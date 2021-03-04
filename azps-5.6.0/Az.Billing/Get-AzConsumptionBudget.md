---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: 70f7f9c43612f1fd1248e019d970d157fadab000
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910541"
---
# <span data-ttu-id="a7f0c-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="a7f0c-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="a7f0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f0c-103">取得訂閱或資源群組中的預算清單。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="a7f0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7f0c-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="a7f0c-105">描述</span><span class="sxs-lookup"><span data-stu-id="a7f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f0c-106">Cmdlet Get-AzConsumptionBudget訂閱或資源群組中的預算清單。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="a7f0c-107">例子</span><span class="sxs-lookup"><span data-stu-id="a7f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f0c-108">範例 1：取得訂閱層級的預算清單</span><span class="sxs-lookup"><span data-stu-id="a7f0c-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="a7f0c-109">範例 2：取得資源群組層級的預算清單</span><span class="sxs-lookup"><span data-stu-id="a7f0c-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="a7f0c-110">範例 3：在訂閱層級使用預算名稱取得預算</span><span class="sxs-lookup"><span data-stu-id="a7f0c-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="a7f0c-111">範例 4：使用資源群組層級的預算名稱取得預算</span><span class="sxs-lookup"><span data-stu-id="a7f0c-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="a7f0c-112">參數</span><span class="sxs-lookup"><span data-stu-id="a7f0c-112">PARAMETERS</span></span>

### <span data-ttu-id="a7f0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f0c-113">-DefaultProfile</span></span>
<span data-ttu-id="a7f0c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f0c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7f0c-115">-Name</span></span>
<span data-ttu-id="a7f0c-116">預算名稱。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-116">Name of a budget.</span></span>

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

### <span data-ttu-id="a7f0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7f0c-118">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="a7f0c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f0c-119">CommonParameters</span></span>
<span data-ttu-id="a7f0c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f0c-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7f0c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f0c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a7f0c-122">INPUTS</span></span>

### <span data-ttu-id="a7f0c-123">沒有</span><span class="sxs-lookup"><span data-stu-id="a7f0c-123">None</span></span>

## <span data-ttu-id="a7f0c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a7f0c-124">OUTPUTS</span></span>

### <span data-ttu-id="a7f0c-125">Microsoft.Azure.Commands.Consumption.models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="a7f0c-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="a7f0c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a7f0c-126">NOTES</span></span>

## <span data-ttu-id="a7f0c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7f0c-127">RELATED LINKS</span></span>
