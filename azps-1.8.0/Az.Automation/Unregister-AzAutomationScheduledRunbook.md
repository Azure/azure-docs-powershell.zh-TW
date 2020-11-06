---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 203573856740e0e155e7dff0755ecad1b5399440
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622925"
---
# <span data-ttu-id="20982-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="20982-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="20982-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20982-102">SYNOPSIS</span></span>
<span data-ttu-id="20982-103">移除 [runbook] 與 [排程] 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="20982-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="20982-104">句法</span><span class="sxs-lookup"><span data-stu-id="20982-104">SYNTAX</span></span>

### <span data-ttu-id="20982-105">ByJobScheduleId (預設) </span><span class="sxs-lookup"><span data-stu-id="20982-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20982-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="20982-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20982-107">說明</span><span class="sxs-lookup"><span data-stu-id="20982-107">DESCRIPTION</span></span>
<span data-ttu-id="20982-108">[ **登出 AzAutomationScheduledRunbook** ] Cmdlet 會移除 Azure 自動化 runbook 和排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="20982-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="20982-109">[排程] 不會再啟動 runbook。</span><span class="sxs-lookup"><span data-stu-id="20982-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="20982-110">示例</span><span class="sxs-lookup"><span data-stu-id="20982-110">EXAMPLES</span></span>

### <span data-ttu-id="20982-111">範例1：移除 [runbook] 與 [排程] 之間的關聯</span><span class="sxs-lookup"><span data-stu-id="20982-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="20982-112">這個命令會移除名為 Runbk01 的 runbook 與名為 Runbk01Sched 的排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="20982-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="20982-113">參數</span><span class="sxs-lookup"><span data-stu-id="20982-113">PARAMETERS</span></span>

### <span data-ttu-id="20982-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20982-114">-AutomationAccountName</span></span>
<span data-ttu-id="20982-115">指定此 Cmdlet 在其上執行的 runbook 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="20982-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="20982-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20982-116">-DefaultProfile</span></span>
<span data-ttu-id="20982-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="20982-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20982-118">-Force</span><span class="sxs-lookup"><span data-stu-id="20982-118">-Force</span></span>
<span data-ttu-id="20982-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="20982-119">ps_force</span></span>

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

### <span data-ttu-id="20982-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="20982-120">-JobScheduleId</span></span>
<span data-ttu-id="20982-121">指定排程的 runbook ID。</span><span class="sxs-lookup"><span data-stu-id="20982-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20982-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20982-122">-ResourceGroupName</span></span>
<span data-ttu-id="20982-123">指定排程的 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="20982-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="20982-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="20982-124">-RunbookName</span></span>
<span data-ttu-id="20982-125">指定此 Cmdlet 從排程 dissociates 的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="20982-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20982-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="20982-126">-ScheduleName</span></span>
<span data-ttu-id="20982-127">指定此 Cmdlet dissociates runbook 所用的排程名稱。</span><span class="sxs-lookup"><span data-stu-id="20982-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20982-128">-確認</span><span class="sxs-lookup"><span data-stu-id="20982-128">-Confirm</span></span>
<span data-ttu-id="20982-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20982-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20982-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20982-130">-WhatIf</span></span>
<span data-ttu-id="20982-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20982-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20982-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20982-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20982-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20982-133">CommonParameters</span></span>
<span data-ttu-id="20982-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20982-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20982-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20982-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20982-136">輸入</span><span class="sxs-lookup"><span data-stu-id="20982-136">INPUTS</span></span>

### <span data-ttu-id="20982-137">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20982-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="20982-138">System.object</span><span class="sxs-lookup"><span data-stu-id="20982-138">System.String</span></span>

## <span data-ttu-id="20982-139">輸出</span><span class="sxs-lookup"><span data-stu-id="20982-139">OUTPUTS</span></span>

### <span data-ttu-id="20982-140">System.void</span><span class="sxs-lookup"><span data-stu-id="20982-140">System.Void</span></span>

## <span data-ttu-id="20982-141">筆記</span><span class="sxs-lookup"><span data-stu-id="20982-141">NOTES</span></span>

## <span data-ttu-id="20982-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="20982-142">RELATED LINKS</span></span>

[<span data-ttu-id="20982-143">AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="20982-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="20982-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="20982-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


