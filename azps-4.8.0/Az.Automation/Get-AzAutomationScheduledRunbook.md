---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128593"
---
# <span data-ttu-id="2ef15-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2ef15-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="2ef15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ef15-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef15-103">取得自動化 runbook 及相關聯的排程。</span><span class="sxs-lookup"><span data-stu-id="2ef15-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="2ef15-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ef15-104">SYNTAX</span></span>

### <span data-ttu-id="2ef15-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="2ef15-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ef15-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="2ef15-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ef15-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="2ef15-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ef15-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="2ef15-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ef15-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="2ef15-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ef15-110">說明</span><span class="sxs-lookup"><span data-stu-id="2ef15-110">DESCRIPTION</span></span>
<span data-ttu-id="2ef15-111">AzAutomationScheduledRunbook Cmdlet 會取得一或多個 Azure 自動化 runbook 及相關聯 **的** 時程表。</span><span class="sxs-lookup"><span data-stu-id="2ef15-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="2ef15-112">根據預設，這個 Cmdlet 會取得所有排程的 runbook。</span><span class="sxs-lookup"><span data-stu-id="2ef15-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="2ef15-113">指定 runbook 或排程的名稱，或兩者來查看特定的 runbook 排程。</span><span class="sxs-lookup"><span data-stu-id="2ef15-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="2ef15-114">示例</span><span class="sxs-lookup"><span data-stu-id="2ef15-114">EXAMPLES</span></span>

### <span data-ttu-id="2ef15-115">範例1：取得所有排程的 runbook</span><span class="sxs-lookup"><span data-stu-id="2ef15-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2ef15-116">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中所有已排程的 runbook。</span><span class="sxs-lookup"><span data-stu-id="2ef15-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="2ef15-117">範例2：取得與 runbook 相關聯的所有排程</span><span class="sxs-lookup"><span data-stu-id="2ef15-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="2ef15-118">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中的 runbook Runbk01 取得所有排程的 runbook。</span><span class="sxs-lookup"><span data-stu-id="2ef15-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="2ef15-119">範例3：取得與排程相關的所有 runbook</span><span class="sxs-lookup"><span data-stu-id="2ef15-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="2ef15-120">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中取得排程 Schedule01 的所有排程 runbook。</span><span class="sxs-lookup"><span data-stu-id="2ef15-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2ef15-121">參數</span><span class="sxs-lookup"><span data-stu-id="2ef15-121">PARAMETERS</span></span>

### <span data-ttu-id="2ef15-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2ef15-122">-AutomationAccountName</span></span>
<span data-ttu-id="2ef15-123">指定此 Cmdlet 在其上執行的 runbook 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="2ef15-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2ef15-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef15-124">-DefaultProfile</span></span>
<span data-ttu-id="2ef15-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ef15-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ef15-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="2ef15-126">-JobScheduleId</span></span>
<span data-ttu-id="2ef15-127">指定此 Cmdlet 取得的排程作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ef15-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ef15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef15-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ef15-129">指定此 Cmdlet 所取得之排程的 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef15-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ef15-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2ef15-130">-RunbookName</span></span>
<span data-ttu-id="2ef15-131">指定此 Cmdlet 取得排程 runbook 的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef15-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="2ef15-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="2ef15-132">-ScheduleName</span></span>
<span data-ttu-id="2ef15-133">指定此 Cmdlet 取得排程 runbook 的排程名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef15-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="2ef15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef15-134">CommonParameters</span></span>
<span data-ttu-id="2ef15-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ef15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef15-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ef15-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef15-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2ef15-137">INPUTS</span></span>

### <span data-ttu-id="2ef15-138">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ef15-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2ef15-139">System.object</span><span class="sxs-lookup"><span data-stu-id="2ef15-139">System.String</span></span>

## <span data-ttu-id="2ef15-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2ef15-140">OUTPUTS</span></span>

### <span data-ttu-id="2ef15-141">JobSchedule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ef15-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="2ef15-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2ef15-142">NOTES</span></span>

## <span data-ttu-id="2ef15-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ef15-143">RELATED LINKS</span></span>

[<span data-ttu-id="2ef15-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2ef15-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="2ef15-145">取消註冊-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2ef15-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


