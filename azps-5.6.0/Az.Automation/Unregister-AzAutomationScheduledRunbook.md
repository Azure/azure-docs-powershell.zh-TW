---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 68f86795a36e605457982898b24cd6dab878ee1f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917430"
---
# <span data-ttu-id="2d824-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2d824-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="2d824-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d824-102">SYNOPSIS</span></span>
<span data-ttu-id="2d824-103">移除執行簿和排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="2d824-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="2d824-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d824-104">SYNTAX</span></span>

### <span data-ttu-id="2d824-105">ByJobScheduleId (預設) </span><span class="sxs-lookup"><span data-stu-id="2d824-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d824-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="2d824-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d824-107">描述</span><span class="sxs-lookup"><span data-stu-id="2d824-107">DESCRIPTION</span></span>
<span data-ttu-id="2d824-108">取消 **註冊-AzAutomationScheduledRunbook** Cmdlet 會移除 Azure 自動化執行手冊和排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="2d824-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="2d824-109">排程不會再啟動執行簿。</span><span class="sxs-lookup"><span data-stu-id="2d824-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="2d824-110">例子</span><span class="sxs-lookup"><span data-stu-id="2d824-110">EXAMPLES</span></span>

### <span data-ttu-id="2d824-111">範例 1：移除 runbook 與排程之間的關聯</span><span class="sxs-lookup"><span data-stu-id="2d824-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="2d824-112">此命令會移除名為 Runbk01 的 Runbook 與名為 Runbk01Sched 的排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="2d824-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="2d824-113">參數</span><span class="sxs-lookup"><span data-stu-id="2d824-113">PARAMETERS</span></span>

### <span data-ttu-id="2d824-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d824-114">-AutomationAccountName</span></span>
<span data-ttu-id="2d824-115">指定此 Cmdlet 操作之 Runbook 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d824-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d824-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d824-116">-DefaultProfile</span></span>
<span data-ttu-id="2d824-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2d824-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d824-118">-強制</span><span class="sxs-lookup"><span data-stu-id="2d824-118">-Force</span></span>
<span data-ttu-id="2d824-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="2d824-119">ps_force</span></span>

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

### <span data-ttu-id="2d824-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="2d824-120">-JobScheduleId</span></span>
<span data-ttu-id="2d824-121">指定已排程 runbook 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d824-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="2d824-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d824-122">-ResourceGroupName</span></span>
<span data-ttu-id="2d824-123">指定已排程 runbook 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2d824-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="2d824-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2d824-124">-RunbookName</span></span>
<span data-ttu-id="2d824-125">指定此 Cmdlet 與排程取消關聯的執行簿名稱。</span><span class="sxs-lookup"><span data-stu-id="2d824-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="2d824-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="2d824-126">-ScheduleName</span></span>
<span data-ttu-id="2d824-127">指定此 Cmdlet 解除關聯 runbook 的排程名稱。</span><span class="sxs-lookup"><span data-stu-id="2d824-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="2d824-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2d824-128">-Confirm</span></span>
<span data-ttu-id="2d824-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2d824-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d824-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d824-130">-WhatIf</span></span>
<span data-ttu-id="2d824-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d824-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d824-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d824-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d824-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d824-133">CommonParameters</span></span>
<span data-ttu-id="2d824-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d824-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d824-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2d824-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d824-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2d824-136">INPUTS</span></span>

### <span data-ttu-id="2d824-137">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d824-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2d824-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2d824-138">System.String</span></span>

## <span data-ttu-id="2d824-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2d824-139">OUTPUTS</span></span>

### <span data-ttu-id="2d824-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="2d824-140">System.Void</span></span>

## <span data-ttu-id="2d824-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2d824-141">NOTES</span></span>

## <span data-ttu-id="2d824-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d824-142">RELATED LINKS</span></span>

[<span data-ttu-id="2d824-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2d824-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="2d824-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2d824-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


