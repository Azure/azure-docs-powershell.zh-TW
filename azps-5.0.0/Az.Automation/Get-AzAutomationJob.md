---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140566"
---
# <span data-ttu-id="d37cc-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d37cc-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="d37cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d37cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d37cc-103">取得自動化 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="d37cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="d37cc-104">SYNTAX</span></span>

### <span data-ttu-id="d37cc-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="d37cc-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d37cc-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="d37cc-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d37cc-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d37cc-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d37cc-108">說明</span><span class="sxs-lookup"><span data-stu-id="d37cc-108">DESCRIPTION</span></span>
<span data-ttu-id="d37cc-109">**AzAutomationJob** Cmdlet 會取得 Azure 自動化中的 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="d37cc-110">示例</span><span class="sxs-lookup"><span data-stu-id="d37cc-110">EXAMPLES</span></span>

### <span data-ttu-id="d37cc-111">範例1：取得特定的 runbook 作業</span><span class="sxs-lookup"><span data-stu-id="d37cc-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="d37cc-112">這個命令會取得具有指定 GUID 的作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="d37cc-113">範例2：取得 runbook 的所有作業</span><span class="sxs-lookup"><span data-stu-id="d37cc-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="d37cc-114">這個命令會取得與名為 Runbook02 的 runbook 相關聯的所有作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="d37cc-115">範例3：取得所有執行中的作業</span><span class="sxs-lookup"><span data-stu-id="d37cc-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="d37cc-116">這個命令會取得自動帳戶（名為 Contoso17）中所有執行中的作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d37cc-117">參數</span><span class="sxs-lookup"><span data-stu-id="d37cc-117">PARAMETERS</span></span>

### <span data-ttu-id="d37cc-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d37cc-118">-AutomationAccountName</span></span>
<span data-ttu-id="d37cc-119">指定此 Cmdlet 取得作業之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d37cc-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="d37cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37cc-120">-DefaultProfile</span></span>
<span data-ttu-id="d37cc-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d37cc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d37cc-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d37cc-122">-EndTime</span></span>
<span data-ttu-id="d37cc-123">將作業的結束時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="d37cc-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="d37cc-124">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="d37cc-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="d37cc-125">這個 Cmdlet 會取得在此參數指定的值上或之前有結束時間的作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37cc-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d37cc-126">-Id</span></span>
<span data-ttu-id="d37cc-127">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d37cc-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37cc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37cc-128">-ResourceGroupName</span></span>
<span data-ttu-id="d37cc-129">指定此 Cmdlet 在其中取得作業的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d37cc-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="d37cc-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d37cc-130">-RunbookName</span></span>
<span data-ttu-id="d37cc-131">指定此 Cmdlet 取得作業的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="d37cc-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37cc-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d37cc-132">-StartTime</span></span>
<span data-ttu-id="d37cc-133">將作業的開始時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="d37cc-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="d37cc-134">這個 Cmdlet 會取得在此參數指定的值或其之後有開始時間的作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37cc-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="d37cc-135">-Status</span></span>
<span data-ttu-id="d37cc-136">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="d37cc-136">Specifies the status of a job.</span></span>
<span data-ttu-id="d37cc-137">這個 Cmdlet 會取得狀態與此參數相符的作業。</span><span class="sxs-lookup"><span data-stu-id="d37cc-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="d37cc-138">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d37cc-138">Valid values are:</span></span> 
- <span data-ttu-id="d37cc-139">啟用</span><span class="sxs-lookup"><span data-stu-id="d37cc-139">Activating</span></span>
- <span data-ttu-id="d37cc-140">完畢</span><span class="sxs-lookup"><span data-stu-id="d37cc-140">Completed</span></span>
- <span data-ttu-id="d37cc-141">成功</span><span class="sxs-lookup"><span data-stu-id="d37cc-141">Failed</span></span>
- <span data-ttu-id="d37cc-142">排</span><span class="sxs-lookup"><span data-stu-id="d37cc-142">Queued</span></span>
- <span data-ttu-id="d37cc-143">開始</span><span class="sxs-lookup"><span data-stu-id="d37cc-143">Resuming</span></span>
- <span data-ttu-id="d37cc-144">進行</span><span class="sxs-lookup"><span data-stu-id="d37cc-144">Running</span></span>
- <span data-ttu-id="d37cc-145">入門</span><span class="sxs-lookup"><span data-stu-id="d37cc-145">Starting</span></span>
- <span data-ttu-id="d37cc-146">被</span><span class="sxs-lookup"><span data-stu-id="d37cc-146">Stopped</span></span>
- <span data-ttu-id="d37cc-147">終止</span><span class="sxs-lookup"><span data-stu-id="d37cc-147">Stopping</span></span>
- <span data-ttu-id="d37cc-148">封存</span><span class="sxs-lookup"><span data-stu-id="d37cc-148">Suspended</span></span>
- <span data-ttu-id="d37cc-149">封存</span><span class="sxs-lookup"><span data-stu-id="d37cc-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37cc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37cc-150">CommonParameters</span></span>
<span data-ttu-id="d37cc-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d37cc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37cc-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d37cc-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37cc-153">輸入</span><span class="sxs-lookup"><span data-stu-id="d37cc-153">INPUTS</span></span>

### <span data-ttu-id="d37cc-154">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="d37cc-154">System.Guid</span></span>

### <span data-ttu-id="d37cc-155">System.object</span><span class="sxs-lookup"><span data-stu-id="d37cc-155">System.String</span></span>

## <span data-ttu-id="d37cc-156">輸出</span><span class="sxs-lookup"><span data-stu-id="d37cc-156">OUTPUTS</span></span>

### <span data-ttu-id="d37cc-157">[作為] 的 [自動化] 工作</span><span class="sxs-lookup"><span data-stu-id="d37cc-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="d37cc-158">筆記</span><span class="sxs-lookup"><span data-stu-id="d37cc-158">NOTES</span></span>

## <span data-ttu-id="d37cc-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="d37cc-159">RELATED LINKS</span></span>

[<span data-ttu-id="d37cc-160">AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d37cc-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="d37cc-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d37cc-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="d37cc-162">停止 AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d37cc-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="d37cc-163">暫停-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d37cc-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


