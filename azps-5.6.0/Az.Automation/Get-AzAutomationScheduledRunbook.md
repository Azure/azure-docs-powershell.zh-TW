---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6dfe33146ba2e35c728211f7f4b17fcfccf40ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917473"
---
# <span data-ttu-id="677d9-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="677d9-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="677d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="677d9-102">SYNOPSIS</span></span>
<span data-ttu-id="677d9-103">獲得自動化執行手冊及相關排程。</span><span class="sxs-lookup"><span data-stu-id="677d9-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="677d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="677d9-104">SYNTAX</span></span>

### <span data-ttu-id="677d9-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="677d9-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677d9-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="677d9-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677d9-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="677d9-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677d9-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="677d9-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677d9-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="677d9-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="677d9-110">描述</span><span class="sxs-lookup"><span data-stu-id="677d9-110">DESCRIPTION</span></span>
<span data-ttu-id="677d9-111">**Get-AzAutomationScheduledRunbook** Cmdlet 會取得一或多個 Azure 自動化執行手冊及相關排程。</span><span class="sxs-lookup"><span data-stu-id="677d9-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="677d9-112">根據預設，此 Cmdlet 會獲得所有排定的 runbook。</span><span class="sxs-lookup"><span data-stu-id="677d9-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="677d9-113">指定 runbook 或排程的名稱，或兩者同時查看特定的 runbook 排程。</span><span class="sxs-lookup"><span data-stu-id="677d9-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="677d9-114">例子</span><span class="sxs-lookup"><span data-stu-id="677d9-114">EXAMPLES</span></span>

### <span data-ttu-id="677d9-115">範例 1：取得所有排程的 runbooks</span><span class="sxs-lookup"><span data-stu-id="677d9-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="677d9-116">此命令會獲得 Azure Automation 帳戶中名為 Contoso17 的所有已排程 runbook。</span><span class="sxs-lookup"><span data-stu-id="677d9-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="677d9-117">範例 2：取得與 runbook 關聯的所有排程</span><span class="sxs-lookup"><span data-stu-id="677d9-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="677d9-118">此命令會獲得 Azure Automation 帳戶 Contoso17 中 runbook Runbk01 的所有排程 runbook。</span><span class="sxs-lookup"><span data-stu-id="677d9-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="677d9-119">範例 3：取得與排程相關聯的所有 runbooks</span><span class="sxs-lookup"><span data-stu-id="677d9-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="677d9-120">此命令會獲得 Azure Automation 帳戶 Contoso17 中排程的所有排程執行簿。</span><span class="sxs-lookup"><span data-stu-id="677d9-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="677d9-121">參數</span><span class="sxs-lookup"><span data-stu-id="677d9-121">PARAMETERS</span></span>

### <span data-ttu-id="677d9-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="677d9-122">-AutomationAccountName</span></span>
<span data-ttu-id="677d9-123">指定此 Cmdlet 操作之 Runbook 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="677d9-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="677d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677d9-124">-DefaultProfile</span></span>
<span data-ttu-id="677d9-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="677d9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="677d9-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="677d9-126">-JobScheduleId</span></span>
<span data-ttu-id="677d9-127">指定此 Cmdlet 所獲得已排程工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="677d9-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="677d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="677d9-129">指定此 Cmdlet 所獲得之已排程 runbook 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="677d9-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="677d9-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="677d9-130">-RunbookName</span></span>
<span data-ttu-id="677d9-131">指定此 Cmdlet 可排程 runbooks 的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="677d9-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677d9-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="677d9-132">-ScheduleName</span></span>
<span data-ttu-id="677d9-133">指定此 Cmdlet 可排程 runbook 的排程名稱。</span><span class="sxs-lookup"><span data-stu-id="677d9-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677d9-134">CommonParameters</span></span>
<span data-ttu-id="677d9-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="677d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677d9-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="677d9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677d9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="677d9-137">INPUTS</span></span>

### <span data-ttu-id="677d9-138">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="677d9-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="677d9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="677d9-139">System.String</span></span>

## <span data-ttu-id="677d9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="677d9-140">OUTPUTS</span></span>

### <span data-ttu-id="677d9-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="677d9-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="677d9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="677d9-142">NOTES</span></span>

## <span data-ttu-id="677d9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="677d9-143">RELATED LINKS</span></span>

[<span data-ttu-id="677d9-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="677d9-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="677d9-145">未註冊-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="677d9-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


