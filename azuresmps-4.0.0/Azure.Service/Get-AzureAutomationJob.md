---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967815"
---
# <span data-ttu-id="2d091-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2d091-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="2d091-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d091-102">SYNOPSIS</span></span>

<span data-ttu-id="2d091-103">取得一或多個 Azure 自動化 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="2d091-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="2d091-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d091-104">SYNTAX</span></span>

### <span data-ttu-id="2d091-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="2d091-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2d091-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="2d091-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d091-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="2d091-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2d091-108">說明</span><span class="sxs-lookup"><span data-stu-id="2d091-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2d091-109">**AzureAutomationJob** Cmdlet 會在 Microsoft Azure 自動化中取得一或多個 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="2d091-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="2d091-110">示例</span><span class="sxs-lookup"><span data-stu-id="2d091-110">EXAMPLES</span></span>

### <span data-ttu-id="2d091-111">範例1：取得特定的 runbook 作業</span><span class="sxs-lookup"><span data-stu-id="2d091-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="2d091-112">這個命令會取得具有指定 GUID 的作業。</span><span class="sxs-lookup"><span data-stu-id="2d091-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="2d091-113">範例2：取得 runbook 的所有作業</span><span class="sxs-lookup"><span data-stu-id="2d091-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="2d091-114">這個命令會取得與名為 MyRunbook 的 runbook 相關聯的所有作業。</span><span class="sxs-lookup"><span data-stu-id="2d091-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="2d091-115">範例2：取得所有執行中的作業</span><span class="sxs-lookup"><span data-stu-id="2d091-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="2d091-116">這個命令會取得自動化帳戶中名稱為 Contoso17 的所有執行中作業。</span><span class="sxs-lookup"><span data-stu-id="2d091-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="2d091-117">參數</span><span class="sxs-lookup"><span data-stu-id="2d091-117">PARAMETERS</span></span>

### <span data-ttu-id="2d091-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d091-118">-AutomationAccountName</span></span>
<span data-ttu-id="2d091-119">指定 Azure 自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d091-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="2d091-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2d091-120">-EndTime</span></span>
<span data-ttu-id="2d091-121">指定作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="2d091-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d091-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2d091-122">-Id</span></span>
<span data-ttu-id="2d091-123">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d091-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d091-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2d091-124">-Profile</span></span>
<span data-ttu-id="2d091-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2d091-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d091-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2d091-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d091-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2d091-127">-RunbookName</span></span>
<span data-ttu-id="2d091-128">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d091-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d091-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2d091-129">-StartTime</span></span>
<span data-ttu-id="2d091-130">指定作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="2d091-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d091-131">-狀態</span><span class="sxs-lookup"><span data-stu-id="2d091-131">-Status</span></span>
<span data-ttu-id="2d091-132">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d091-132">Specifies the status of a job.</span></span>
<span data-ttu-id="2d091-133">這個 Cmdlet 會取得狀態與此參數相符的作業。</span><span class="sxs-lookup"><span data-stu-id="2d091-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="2d091-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2d091-134">Valid values are:</span></span> 

- <span data-ttu-id="2d091-135">完畢</span><span class="sxs-lookup"><span data-stu-id="2d091-135">Completed</span></span>
- <span data-ttu-id="2d091-136">成功</span><span class="sxs-lookup"><span data-stu-id="2d091-136">Failed</span></span>
- <span data-ttu-id="2d091-137">排</span><span class="sxs-lookup"><span data-stu-id="2d091-137">Queued</span></span>
- <span data-ttu-id="2d091-138">入門</span><span class="sxs-lookup"><span data-stu-id="2d091-138">Starting</span></span>
- <span data-ttu-id="2d091-139">開始</span><span class="sxs-lookup"><span data-stu-id="2d091-139">Resuming</span></span>
- <span data-ttu-id="2d091-140">進行</span><span class="sxs-lookup"><span data-stu-id="2d091-140">Running</span></span>
- <span data-ttu-id="2d091-141">被</span><span class="sxs-lookup"><span data-stu-id="2d091-141">Stopped</span></span>
- <span data-ttu-id="2d091-142">終止</span><span class="sxs-lookup"><span data-stu-id="2d091-142">Stopping</span></span>
- <span data-ttu-id="2d091-143">封存</span><span class="sxs-lookup"><span data-stu-id="2d091-143">Suspended</span></span>
- <span data-ttu-id="2d091-144">封存</span><span class="sxs-lookup"><span data-stu-id="2d091-144">Suspending</span></span>
- <span data-ttu-id="2d091-145">啟用</span><span class="sxs-lookup"><span data-stu-id="2d091-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d091-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d091-146">CommonParameters</span></span>
<span data-ttu-id="2d091-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d091-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d091-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d091-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d091-149">輸入</span><span class="sxs-lookup"><span data-stu-id="2d091-149">INPUTS</span></span>

## <span data-ttu-id="2d091-150">輸出</span><span class="sxs-lookup"><span data-stu-id="2d091-150">OUTPUTS</span></span>

### <span data-ttu-id="2d091-151">[作為] 的 [自動化] 工作</span><span class="sxs-lookup"><span data-stu-id="2d091-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="2d091-152">筆記</span><span class="sxs-lookup"><span data-stu-id="2d091-152">NOTES</span></span>

## <span data-ttu-id="2d091-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d091-153">RELATED LINKS</span></span>

[<span data-ttu-id="2d091-154">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2d091-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="2d091-155">停止 AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2d091-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="2d091-156">暫停-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="2d091-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


