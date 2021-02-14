---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130062"
---
# <span data-ttu-id="037c7-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="037c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="037c7-102">SYNOPSIS</span></span>
<span data-ttu-id="037c7-103">啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="037c7-103">Starts a runbook job.</span></span>

## <span data-ttu-id="037c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="037c7-104">SYNTAX</span></span>

### <span data-ttu-id="037c7-105">ByAsynchronousReturnJob (預設) </span><span class="sxs-lookup"><span data-stu-id="037c7-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="037c7-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="037c7-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="037c7-107">說明</span><span class="sxs-lookup"><span data-stu-id="037c7-107">DESCRIPTION</span></span>
<span data-ttu-id="037c7-108">**AzAutomationRunbook** Cmdlet 會啟動 Azure 自動化 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="037c7-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="037c7-109">指定 runbook 的識別碼或名稱。</span><span class="sxs-lookup"><span data-stu-id="037c7-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="037c7-110">示例</span><span class="sxs-lookup"><span data-stu-id="037c7-110">EXAMPLES</span></span>

### <span data-ttu-id="037c7-111">範例1：啟動 runbook 作業</span><span class="sxs-lookup"><span data-stu-id="037c7-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="037c7-112">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 Runbk01 的 runbook 啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="037c7-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="037c7-113">範例2：使用參數開始 Python 2 runbook 作業</span><span class="sxs-lookup"><span data-stu-id="037c7-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="037c7-114">這個命令會在 Azure 自動化帳戶（名為 "ValueForPosition1"）中，以 "" 做為第二個位置參數，以 "ValueForPosition2" 為開頭的 Python 2 runbook 啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="037c7-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="037c7-115">範例3：啟動 runbook 作業並等待結果</span><span class="sxs-lookup"><span data-stu-id="037c7-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="037c7-116">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 Runbk01 的 runbook 啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="037c7-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="037c7-117">這個命令會指定 _Wait_ 參數。</span><span class="sxs-lookup"><span data-stu-id="037c7-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="037c7-118">因此，它會在作業完成後傳回結果。</span><span class="sxs-lookup"><span data-stu-id="037c7-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="037c7-119">此 Cmdlet 會在結果中等待1000秒。</span><span class="sxs-lookup"><span data-stu-id="037c7-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="037c7-120">參數</span><span class="sxs-lookup"><span data-stu-id="037c7-120">PARAMETERS</span></span>

### <span data-ttu-id="037c7-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="037c7-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="037c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037c7-122">-DefaultProfile</span></span>
<span data-ttu-id="037c7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="037c7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="037c7-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="037c7-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="037c7-125">指定此 Cmdlet 在放棄工作之前等待作業完成的秒數。</span><span class="sxs-lookup"><span data-stu-id="037c7-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="037c7-126">預設值為10800或3小時。</span><span class="sxs-lookup"><span data-stu-id="037c7-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="037c7-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c7-128">-參數</span><span class="sxs-lookup"><span data-stu-id="037c7-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="037c7-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="037c7-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="037c7-130">-RunOn</span></span>
<span data-ttu-id="037c7-131">指定要在哪個混合式輔助角色群組上執行 runbook。</span><span class="sxs-lookup"><span data-stu-id="037c7-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c7-132">-稍候</span><span class="sxs-lookup"><span data-stu-id="037c7-132">-Wait</span></span>
<span data-ttu-id="037c7-133">表示此 Cmdlet 會等待作業完成、暫停或失敗，然後將控制權傳回給 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="037c7-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037c7-134">CommonParameters</span></span>
<span data-ttu-id="037c7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="037c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037c7-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="037c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037c7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="037c7-137">INPUTS</span></span>

### <span data-ttu-id="037c7-138">System.object</span><span class="sxs-lookup"><span data-stu-id="037c7-138">System.String</span></span>

## <span data-ttu-id="037c7-139">輸出</span><span class="sxs-lookup"><span data-stu-id="037c7-139">OUTPUTS</span></span>

### <span data-ttu-id="037c7-140">[作為] 的 [自動化] 工作</span><span class="sxs-lookup"><span data-stu-id="037c7-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="037c7-141">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="037c7-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="037c7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="037c7-142">NOTES</span></span>

## <span data-ttu-id="037c7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="037c7-143">RELATED LINKS</span></span>

[<span data-ttu-id="037c7-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-145">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-146">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-147">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-148">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-149">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-150">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="037c7-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="037c7-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
