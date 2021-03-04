---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: da687cc3831f4a3cb278dbf032905b39750b8c8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915645"
---
# <span data-ttu-id="a815d-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a815d-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="a815d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a815d-102">SYNOPSIS</span></span>
<span data-ttu-id="a815d-103">刪除自動化排程。</span><span class="sxs-lookup"><span data-stu-id="a815d-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="a815d-104">語法</span><span class="sxs-lookup"><span data-stu-id="a815d-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a815d-105">描述</span><span class="sxs-lookup"><span data-stu-id="a815d-105">DESCRIPTION</span></span>
<span data-ttu-id="a815d-106">**Remove-AzAutomationSchedule** Cmdlet 會從 Azure Automation 中刪除排程。</span><span class="sxs-lookup"><span data-stu-id="a815d-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="a815d-107">例子</span><span class="sxs-lookup"><span data-stu-id="a815d-107">EXAMPLES</span></span>

### <span data-ttu-id="a815d-108">範例 1：移除排程</span><span class="sxs-lookup"><span data-stu-id="a815d-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a815d-109">此命令會刪除資源群組 ResourceGroup01 中自動化帳戶 Contoso17 中名為 Schedule01 的排程。</span><span class="sxs-lookup"><span data-stu-id="a815d-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a815d-110">參數</span><span class="sxs-lookup"><span data-stu-id="a815d-110">PARAMETERS</span></span>

### <span data-ttu-id="a815d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a815d-111">-AutomationAccountName</span></span>
<span data-ttu-id="a815d-112">指定此 Cmdlet 移除排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a815d-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a815d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a815d-113">-DefaultProfile</span></span>
<span data-ttu-id="a815d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a815d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a815d-115">-強制</span><span class="sxs-lookup"><span data-stu-id="a815d-115">-Force</span></span>
<span data-ttu-id="a815d-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a815d-116">ps_force</span></span>

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

### <span data-ttu-id="a815d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a815d-117">-Name</span></span>
<span data-ttu-id="a815d-118">指定此 Cmdlet 移除的排程名稱。</span><span class="sxs-lookup"><span data-stu-id="a815d-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a815d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a815d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a815d-120">指定此 Cmdlet 移除排程的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a815d-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a815d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a815d-121">-Confirm</span></span>
<span data-ttu-id="a815d-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a815d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a815d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a815d-123">-WhatIf</span></span>
<span data-ttu-id="a815d-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a815d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a815d-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a815d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a815d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a815d-126">CommonParameters</span></span>
<span data-ttu-id="a815d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a815d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a815d-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a815d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a815d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a815d-129">INPUTS</span></span>

### <span data-ttu-id="a815d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a815d-130">System.String</span></span>

## <span data-ttu-id="a815d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a815d-131">OUTPUTS</span></span>

### <span data-ttu-id="a815d-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="a815d-132">System.Void</span></span>

## <span data-ttu-id="a815d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a815d-133">NOTES</span></span>

## <span data-ttu-id="a815d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a815d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a815d-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a815d-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="a815d-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a815d-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="a815d-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a815d-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


