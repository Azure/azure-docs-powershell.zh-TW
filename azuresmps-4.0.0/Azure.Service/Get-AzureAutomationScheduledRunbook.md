---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967803"
---
# <span data-ttu-id="c4ef1-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c4ef1-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="c4ef1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4ef1-102">SYNOPSIS</span></span>

<span data-ttu-id="c4ef1-103">取得 Azure 自動化 runbook 及相關聯的排程。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="c4ef1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4ef1-104">SYNTAX</span></span>

### <span data-ttu-id="c4ef1-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="c4ef1-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4ef1-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c4ef1-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c4ef1-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c4ef1-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c4ef1-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="c4ef1-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c4ef1-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="c4ef1-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4ef1-110">說明</span><span class="sxs-lookup"><span data-stu-id="c4ef1-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c4ef1-111">AzureAutomationScheduledRunbook 會取得一或多個 Azure 自動化 runbook 及相關聯 **的** 時程表。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="c4ef1-112">根據預設，會傳回所有排程的 runbook。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="c4ef1-113">若要取得特定排程的 runbook，請指定 runbook 名稱和排程名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="c4ef1-114">若要取得與 runbook 相關聯的所有排程，只需指定 runbook 名稱即可。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="c4ef1-115">若要取得與排程相關的所有 runbook，請只指定排程名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="c4ef1-116">示例</span><span class="sxs-lookup"><span data-stu-id="c4ef1-116">EXAMPLES</span></span>

### <span data-ttu-id="c4ef1-117">範例1：取得所有排程的 runbook</span><span class="sxs-lookup"><span data-stu-id="c4ef1-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c4ef1-118">這個命令會取得自動帳戶（名為 Contoso17）中所有排程的 runbook。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c4ef1-119">範例2：取得與 runbook 相關聯的所有排程</span><span class="sxs-lookup"><span data-stu-id="c4ef1-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="c4ef1-120">這個命令會取得名為 Contoso17 之自動化帳戶中 runbook Runbk01 的所有排程 runbook。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c4ef1-121">範例3：取得與排程相關的所有 runbook</span><span class="sxs-lookup"><span data-stu-id="c4ef1-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="c4ef1-122">這個命令會取得名為 Contoso17 之自動化帳戶中排程 Schedule01 的所有排程 runbook。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c4ef1-123">參數</span><span class="sxs-lookup"><span data-stu-id="c4ef1-123">PARAMETERS</span></span>

### <span data-ttu-id="c4ef1-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4ef1-124">-AutomationAccountName</span></span>
<span data-ttu-id="c4ef1-125">指定 Azure 自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-125">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ef1-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c4ef1-126">-JobScheduleId</span></span>
<span data-ttu-id="c4ef1-127">指定排程作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ef1-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c4ef1-128">-Profile</span></span>
<span data-ttu-id="c4ef1-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4ef1-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ef1-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c4ef1-131">-RunbookName</span></span>
<span data-ttu-id="c4ef1-132">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ef1-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="c4ef1-133">-ScheduleName</span></span>
<span data-ttu-id="c4ef1-134">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ef1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ef1-135">CommonParameters</span></span>
<span data-ttu-id="c4ef1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ef1-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4ef1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ef1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c4ef1-138">INPUTS</span></span>

## <span data-ttu-id="c4ef1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c4ef1-139">OUTPUTS</span></span>

### <span data-ttu-id="c4ef1-140">JobSchedule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c4ef1-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="c4ef1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c4ef1-141">NOTES</span></span>

## <span data-ttu-id="c4ef1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4ef1-142">RELATED LINKS</span></span>

[<span data-ttu-id="c4ef1-143">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c4ef1-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="c4ef1-144">取消註冊-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c4ef1-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


