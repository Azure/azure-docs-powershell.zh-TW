---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453820"
---
# <span data-ttu-id="ef632-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="ef632-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="ef632-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef632-102">SYNOPSIS</span></span>
<span data-ttu-id="ef632-103">在訂閱或資源群組中移除預算。</span><span class="sxs-lookup"><span data-stu-id="ef632-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef632-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef632-104">SYNTAX</span></span>

### <span data-ttu-id="ef632-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="ef632-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef632-106">管線</span><span class="sxs-lookup"><span data-stu-id="ef632-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef632-107">說明</span><span class="sxs-lookup"><span data-stu-id="ef632-107">DESCRIPTION</span></span>
<span data-ttu-id="ef632-108">Remove-AzureRmConsumptionBudget Cmdlet 會移除訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="ef632-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ef632-109">示例</span><span class="sxs-lookup"><span data-stu-id="ef632-109">EXAMPLES</span></span>

### <span data-ttu-id="ef632-110">範例1：在訂閱層級移除含預算名稱的預算</span><span class="sxs-lookup"><span data-stu-id="ef632-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="ef632-111">範例2：在資源群組層級移除含預算名稱的預算</span><span class="sxs-lookup"><span data-stu-id="ef632-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="ef632-112">範例3：透過管道在訂閱層級移除預算</span><span class="sxs-lookup"><span data-stu-id="ef632-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="ef632-113">參數</span><span class="sxs-lookup"><span data-stu-id="ef632-113">PARAMETERS</span></span>

### <span data-ttu-id="ef632-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef632-114">-DefaultProfile</span></span>
<span data-ttu-id="ef632-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef632-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef632-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef632-116">-InputObject</span></span>
<span data-ttu-id="ef632-117">預算物件。</span><span class="sxs-lookup"><span data-stu-id="ef632-117">Budget object.</span></span>

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

### <span data-ttu-id="ef632-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef632-118">-Name</span></span>
<span data-ttu-id="ef632-119">預算的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef632-119">Name of a budget.</span></span>

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

### <span data-ttu-id="ef632-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef632-120">-PassThru</span></span>
<span data-ttu-id="ef632-121">如果已成功移除預算，則此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ef632-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="ef632-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef632-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef632-123">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ef632-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="ef632-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ef632-124">-Confirm</span></span>
<span data-ttu-id="ef632-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef632-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef632-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef632-126">-WhatIf</span></span>
<span data-ttu-id="ef632-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef632-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef632-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef632-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef632-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef632-129">CommonParameters</span></span>
<span data-ttu-id="ef632-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef632-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef632-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef632-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef632-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ef632-132">INPUTS</span></span>

### <span data-ttu-id="ef632-133">PSBudget 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef632-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="ef632-134">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ef632-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ef632-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ef632-135">OUTPUTS</span></span>

### <span data-ttu-id="ef632-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ef632-136">System.Boolean</span></span>

## <span data-ttu-id="ef632-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ef632-137">NOTES</span></span>

## <span data-ttu-id="ef632-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef632-138">RELATED LINKS</span></span>
