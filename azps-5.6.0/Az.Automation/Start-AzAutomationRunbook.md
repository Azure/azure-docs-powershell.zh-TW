---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 00eb652bc9779554f1c860edd503fc752c7ccaa0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903342"
---
# <span data-ttu-id="f8bb0-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="f8bb0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bb0-103">啟動 runbook 工作。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-103">Starts a runbook job.</span></span>

## <span data-ttu-id="f8bb0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8bb0-104">SYNTAX</span></span>

### <span data-ttu-id="f8bb0-105">ByAsynchronousReturnJob (預設) </span><span class="sxs-lookup"><span data-stu-id="f8bb0-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8bb0-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="f8bb0-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8bb0-107">描述</span><span class="sxs-lookup"><span data-stu-id="f8bb0-107">DESCRIPTION</span></span>
<span data-ttu-id="f8bb0-108">**Start-AzAutomationRunbook** Cmdlet 會啟動 Azure 自動化 runbook 工作。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="f8bb0-109">指定 runbook 的識別碼或名稱。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="f8bb0-110">例子</span><span class="sxs-lookup"><span data-stu-id="f8bb0-110">EXAMPLES</span></span>

### <span data-ttu-id="f8bb0-111">範例 1：啟動 runbook 工作</span><span class="sxs-lookup"><span data-stu-id="f8bb0-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8bb0-112">此命令會針對 Azure Automation 帳戶中名為 Contoso17 的 Runbk01 runbook 啟動 runbook 工作。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8bb0-113">範例 2：使用參數啟動一個包含參數的Python 2 runbook 工作</span><span class="sxs-lookup"><span data-stu-id="f8bb0-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="f8bb0-114">此命令會啟動名為 Contoso17 的 Azure 自動化帳戶中名為 RunbkPy01 的資料列 2 Runbook 工作，其中第一個位置參數是 "ValueForPosition1"，第二個位置參數是 "ValueForPosition2"。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="f8bb0-115">範例 3：啟動 runbook 工作並等待結果</span><span class="sxs-lookup"><span data-stu-id="f8bb0-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="f8bb0-116">此命令會針對 Azure Automation 帳戶中名為 Contoso17 的 Runbk01 runbook 啟動 runbook 工作。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="f8bb0-117">此命令會指定 _Wait_ 參數。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="f8bb0-118">因此，它會在工作完成之後，返回結果。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="f8bb0-119">Cmdlet 會等候最多 1000 秒以取得結果。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="f8bb0-120">參數</span><span class="sxs-lookup"><span data-stu-id="f8bb0-120">PARAMETERS</span></span>

### <span data-ttu-id="f8bb0-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8bb0-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="f8bb0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bb0-122">-DefaultProfile</span></span>
<span data-ttu-id="f8bb0-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f8bb0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8bb0-124">-MaxWait以秒為單位</span><span class="sxs-lookup"><span data-stu-id="f8bb0-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="f8bb0-125">指定此 Cmdlet 等待工作完成再捨棄工作的秒數。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="f8bb0-126">預設值為 10800 或 3 小時。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="f8bb0-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8bb0-127">-Name</span></span>
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

### <span data-ttu-id="f8bb0-128">-參數</span><span class="sxs-lookup"><span data-stu-id="f8bb0-128">-Parameters</span></span>
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

### <span data-ttu-id="f8bb0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8bb0-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f8bb0-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="f8bb0-130">-RunOn</span></span>
<span data-ttu-id="f8bb0-131">指定執行 runbook 的混合式員工群組。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="f8bb0-132">-等待</span><span class="sxs-lookup"><span data-stu-id="f8bb0-132">-Wait</span></span>
<span data-ttu-id="f8bb0-133">表示此 Cmdlet 會等待工作完成、暫停或失敗，然後將控制權返回 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="f8bb0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bb0-134">CommonParameters</span></span>
<span data-ttu-id="f8bb0-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bb0-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f8bb0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bb0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f8bb0-137">INPUTS</span></span>

### <span data-ttu-id="f8bb0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f8bb0-138">System.String</span></span>

## <span data-ttu-id="f8bb0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f8bb0-139">OUTPUTS</span></span>

### <span data-ttu-id="f8bb0-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="f8bb0-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="f8bb0-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f8bb0-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f8bb0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f8bb0-142">NOTES</span></span>

## <span data-ttu-id="f8bb0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8bb0-143">RELATED LINKS</span></span>

[<span data-ttu-id="f8bb0-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f8bb0-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8bb0-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
