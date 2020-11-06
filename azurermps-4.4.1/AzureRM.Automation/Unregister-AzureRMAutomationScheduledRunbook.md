---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454920"
---
# <span data-ttu-id="dd67b-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="dd67b-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="dd67b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd67b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd67b-103">移除 [runbook] 與 [排程] 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="dd67b-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd67b-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd67b-104">SYNTAX</span></span>

### <span data-ttu-id="dd67b-105">ByJobScheduleId (預設) </span><span class="sxs-lookup"><span data-stu-id="dd67b-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd67b-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="dd67b-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd67b-107">說明</span><span class="sxs-lookup"><span data-stu-id="dd67b-107">DESCRIPTION</span></span>
<span data-ttu-id="dd67b-108">[ **登出 AzureRmAutomationScheduledRunbook** ] Cmdlet 會移除 Azure 自動化 runbook 和排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="dd67b-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="dd67b-109">[排程] 不會再啟動 runbook。</span><span class="sxs-lookup"><span data-stu-id="dd67b-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="dd67b-110">示例</span><span class="sxs-lookup"><span data-stu-id="dd67b-110">EXAMPLES</span></span>

### <span data-ttu-id="dd67b-111">範例1：移除 [runbook] 與 [排程] 之間的關聯</span><span class="sxs-lookup"><span data-stu-id="dd67b-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="dd67b-112">這個命令會移除名為 Runbk01 的 runbook 與名為 Runbk01Sched 的排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="dd67b-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="dd67b-113">參數</span><span class="sxs-lookup"><span data-stu-id="dd67b-113">PARAMETERS</span></span>

### <span data-ttu-id="dd67b-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd67b-114">-AutomationAccountName</span></span>
<span data-ttu-id="dd67b-115">指定此 Cmdlet 在其上執行的 runbook 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd67b-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dd67b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dd67b-116">-Force</span></span>
<span data-ttu-id="dd67b-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="dd67b-117">ps_force</span></span>

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

### <span data-ttu-id="dd67b-118">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="dd67b-118">-JobScheduleId</span></span>
<span data-ttu-id="dd67b-119">指定排程的 runbook ID。</span><span class="sxs-lookup"><span data-stu-id="dd67b-119">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="dd67b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd67b-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd67b-121">指定排程的 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd67b-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="dd67b-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="dd67b-122">-RunbookName</span></span>
<span data-ttu-id="dd67b-123">指定此 Cmdlet 從排程 dissociates 的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="dd67b-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="dd67b-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="dd67b-124">-ScheduleName</span></span>
<span data-ttu-id="dd67b-125">指定此 Cmdlet dissociates runbook 所用的排程名稱。</span><span class="sxs-lookup"><span data-stu-id="dd67b-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="dd67b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="dd67b-126">-Confirm</span></span>
<span data-ttu-id="dd67b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd67b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd67b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd67b-128">-WhatIf</span></span>
<span data-ttu-id="dd67b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd67b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd67b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd67b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd67b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd67b-131">-DefaultProfile</span></span>
<span data-ttu-id="dd67b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd67b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd67b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd67b-133">CommonParameters</span></span>
<span data-ttu-id="dd67b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd67b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd67b-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd67b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd67b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dd67b-136">INPUTS</span></span>

## <span data-ttu-id="dd67b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="dd67b-137">OUTPUTS</span></span>

## <span data-ttu-id="dd67b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="dd67b-138">NOTES</span></span>

## <span data-ttu-id="dd67b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd67b-139">RELATED LINKS</span></span>

[<span data-ttu-id="dd67b-140">AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="dd67b-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="dd67b-141">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="dd67b-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


