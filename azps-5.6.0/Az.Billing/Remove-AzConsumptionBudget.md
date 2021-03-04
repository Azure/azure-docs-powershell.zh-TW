---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 58a4b7be314489a847479692a08f495fcf4c7146
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909778"
---
# <span data-ttu-id="41bb2-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="41bb2-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="41bb2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="41bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="41bb2-103">移除訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="41bb2-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="41bb2-104">語法</span><span class="sxs-lookup"><span data-stu-id="41bb2-104">SYNTAX</span></span>

### <span data-ttu-id="41bb2-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="41bb2-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41bb2-106">管道</span><span class="sxs-lookup"><span data-stu-id="41bb2-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41bb2-107">描述</span><span class="sxs-lookup"><span data-stu-id="41bb2-107">DESCRIPTION</span></span>
<span data-ttu-id="41bb2-108">Cmdlet Remove-AzConsumptionBudget訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="41bb2-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="41bb2-109">例子</span><span class="sxs-lookup"><span data-stu-id="41bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="41bb2-110">範例 1：在訂閱層級移除具有預算名稱的預算</span><span class="sxs-lookup"><span data-stu-id="41bb2-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="41bb2-111">範例 2：在資源群組層級移除具有預算名稱的預算</span><span class="sxs-lookup"><span data-stu-id="41bb2-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="41bb2-112">範例 3：透過訂閱層級的管道移除預算</span><span class="sxs-lookup"><span data-stu-id="41bb2-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="41bb2-113">參數</span><span class="sxs-lookup"><span data-stu-id="41bb2-113">PARAMETERS</span></span>

### <span data-ttu-id="41bb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bb2-114">-DefaultProfile</span></span>
<span data-ttu-id="41bb2-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="41bb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41bb2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41bb2-116">-InputObject</span></span>
<span data-ttu-id="41bb2-117">Budget 物件。</span><span class="sxs-lookup"><span data-stu-id="41bb2-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41bb2-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="41bb2-118">-Name</span></span>
<span data-ttu-id="41bb2-119">預算名稱。</span><span class="sxs-lookup"><span data-stu-id="41bb2-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bb2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41bb2-120">-PassThru</span></span>
<span data-ttu-id="41bb2-121">如果已成功移除預算，Cmdlet 會返回 True。</span><span class="sxs-lookup"><span data-stu-id="41bb2-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bb2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41bb2-122">-ResourceGroupName</span></span>
<span data-ttu-id="41bb2-123">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="41bb2-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bb2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="41bb2-124">-Confirm</span></span>
<span data-ttu-id="41bb2-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="41bb2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bb2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41bb2-126">-WhatIf</span></span>
<span data-ttu-id="41bb2-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41bb2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41bb2-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41bb2-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bb2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bb2-129">CommonParameters</span></span>
<span data-ttu-id="41bb2-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="41bb2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bb2-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="41bb2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bb2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="41bb2-132">INPUTS</span></span>

### <span data-ttu-id="41bb2-133">Microsoft.Azure.Commands.Consumption.models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="41bb2-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="41bb2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="41bb2-134">OUTPUTS</span></span>

### <span data-ttu-id="41bb2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41bb2-135">System.Boolean</span></span>

## <span data-ttu-id="41bb2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="41bb2-136">NOTES</span></span>

## <span data-ttu-id="41bb2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="41bb2-137">RELATED LINKS</span></span>
