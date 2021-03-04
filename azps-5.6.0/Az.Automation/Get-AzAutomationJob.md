---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 378bab1d62d5abcfb1eb2506e41d22bf26b217b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913610"
---
# <span data-ttu-id="063f5-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="063f5-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="063f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="063f5-102">SYNOPSIS</span></span>
<span data-ttu-id="063f5-103">獲得自動化 runbook 工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="063f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="063f5-104">SYNTAX</span></span>

### <span data-ttu-id="063f5-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="063f5-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="063f5-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="063f5-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="063f5-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="063f5-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063f5-108">描述</span><span class="sxs-lookup"><span data-stu-id="063f5-108">DESCRIPTION</span></span>
<span data-ttu-id="063f5-109">**Get-AzAutomationJob** Cmdlet 會取得 Azure Automation 中的 runbook 工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="063f5-110">例子</span><span class="sxs-lookup"><span data-stu-id="063f5-110">EXAMPLES</span></span>

### <span data-ttu-id="063f5-111">範例 1：取得特定的 runbook 工作</span><span class="sxs-lookup"><span data-stu-id="063f5-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="063f5-112">此命令會獲得具有指定 GUID 的工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="063f5-113">範例 2：取得 runbook 的所有工作</span><span class="sxs-lookup"><span data-stu-id="063f5-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="063f5-114">此命令會獲得與 Runbook 名稱為 Runbook02 關聯的所有工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="063f5-115">範例 3：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="063f5-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="063f5-116">此命令會獲得自動化帳戶中名為 Contoso17 的所有執行中工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="063f5-117">參數</span><span class="sxs-lookup"><span data-stu-id="063f5-117">PARAMETERS</span></span>

### <span data-ttu-id="063f5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="063f5-118">-AutomationAccountName</span></span>
<span data-ttu-id="063f5-119">指定此 Cmdlet 可尋找工作的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="063f5-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="063f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063f5-120">-DefaultProfile</span></span>
<span data-ttu-id="063f5-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="063f5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="063f5-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="063f5-122">-EndTime</span></span>
<span data-ttu-id="063f5-123">指定工作的結束時間做為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="063f5-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="063f5-124">您可以指定可以轉換成有效 **DateTimeOffset 的字串**。</span><span class="sxs-lookup"><span data-stu-id="063f5-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="063f5-125">此 Cmdlet 會獲得在此參數指定的值之前結束時間的工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="063f5-126">-Id</span><span class="sxs-lookup"><span data-stu-id="063f5-126">-Id</span></span>
<span data-ttu-id="063f5-127">指定此 Cmdlet 所獲得工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="063f5-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="063f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="063f5-129">指定此 Cmdlet 可工作的資源組名。</span><span class="sxs-lookup"><span data-stu-id="063f5-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="063f5-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="063f5-130">-RunbookName</span></span>
<span data-ttu-id="063f5-131">指定此 Cmdlet 可尋找工作的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="063f5-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="063f5-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="063f5-132">-StartTime</span></span>
<span data-ttu-id="063f5-133">指定工作的開始時間做為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="063f5-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="063f5-134">此 Cmdlet 會獲得在此參數指定值時或之後有開始時間的工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="063f5-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="063f5-135">-Status</span></span>
<span data-ttu-id="063f5-136">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="063f5-136">Specifies the status of a job.</span></span>
<span data-ttu-id="063f5-137">此 Cmdlet 會獲得狀態符合此參數的工作。</span><span class="sxs-lookup"><span data-stu-id="063f5-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="063f5-138">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="063f5-138">Valid values are:</span></span> 
- <span data-ttu-id="063f5-139">啟動</span><span class="sxs-lookup"><span data-stu-id="063f5-139">Activating</span></span>
- <span data-ttu-id="063f5-140">完成</span><span class="sxs-lookup"><span data-stu-id="063f5-140">Completed</span></span>
- <span data-ttu-id="063f5-141">失敗</span><span class="sxs-lookup"><span data-stu-id="063f5-141">Failed</span></span>
- <span data-ttu-id="063f5-142">排隊</span><span class="sxs-lookup"><span data-stu-id="063f5-142">Queued</span></span>
- <span data-ttu-id="063f5-143">恢復</span><span class="sxs-lookup"><span data-stu-id="063f5-143">Resuming</span></span>
- <span data-ttu-id="063f5-144">運行</span><span class="sxs-lookup"><span data-stu-id="063f5-144">Running</span></span>
- <span data-ttu-id="063f5-145">開始</span><span class="sxs-lookup"><span data-stu-id="063f5-145">Starting</span></span>
- <span data-ttu-id="063f5-146">停止</span><span class="sxs-lookup"><span data-stu-id="063f5-146">Stopped</span></span>
- <span data-ttu-id="063f5-147">停止</span><span class="sxs-lookup"><span data-stu-id="063f5-147">Stopping</span></span>
- <span data-ttu-id="063f5-148">暫停</span><span class="sxs-lookup"><span data-stu-id="063f5-148">Suspended</span></span>
- <span data-ttu-id="063f5-149">暫停</span><span class="sxs-lookup"><span data-stu-id="063f5-149">Suspending</span></span>

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

### <span data-ttu-id="063f5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063f5-150">CommonParameters</span></span>
<span data-ttu-id="063f5-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="063f5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063f5-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="063f5-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063f5-153">輸入</span><span class="sxs-lookup"><span data-stu-id="063f5-153">INPUTS</span></span>

### <span data-ttu-id="063f5-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="063f5-154">System.Guid</span></span>

### <span data-ttu-id="063f5-155">System.String</span><span class="sxs-lookup"><span data-stu-id="063f5-155">System.String</span></span>

## <span data-ttu-id="063f5-156">輸出</span><span class="sxs-lookup"><span data-stu-id="063f5-156">OUTPUTS</span></span>

### <span data-ttu-id="063f5-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="063f5-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="063f5-158">筆記</span><span class="sxs-lookup"><span data-stu-id="063f5-158">NOTES</span></span>

## <span data-ttu-id="063f5-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="063f5-159">RELATED LINKS</span></span>

[<span data-ttu-id="063f5-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="063f5-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="063f5-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="063f5-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="063f5-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="063f5-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="063f5-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="063f5-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


