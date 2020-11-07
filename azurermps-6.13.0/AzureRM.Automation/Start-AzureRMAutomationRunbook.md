---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46544d42cb28f5fca046586696b95286cdd7f3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624927"
---
# <span data-ttu-id="10bf9-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="10bf9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="10bf9-103">啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="10bf9-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10bf9-104">句法</span><span class="sxs-lookup"><span data-stu-id="10bf9-104">SYNTAX</span></span>

### <span data-ttu-id="10bf9-105">ByAsynchronousReturnJob (預設) </span><span class="sxs-lookup"><span data-stu-id="10bf9-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10bf9-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="10bf9-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10bf9-107">說明</span><span class="sxs-lookup"><span data-stu-id="10bf9-107">DESCRIPTION</span></span>
<span data-ttu-id="10bf9-108">**AzureRmAutomationRunbook** Cmdlet 會啟動 Azure 自動化 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="10bf9-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="10bf9-109">指定 runbook 的識別碼或名稱。</span><span class="sxs-lookup"><span data-stu-id="10bf9-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="10bf9-110">示例</span><span class="sxs-lookup"><span data-stu-id="10bf9-110">EXAMPLES</span></span>

### <span data-ttu-id="10bf9-111">範例1：啟動 runbook 作業</span><span class="sxs-lookup"><span data-stu-id="10bf9-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="10bf9-112">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 Runbk01 的 runbook 啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="10bf9-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="10bf9-113">範例2：啟動 runbook 作業並等待結果</span><span class="sxs-lookup"><span data-stu-id="10bf9-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="10bf9-114">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 Runbk01 的 runbook 啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="10bf9-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="10bf9-115">這個命令會指定 _Wait_ 參數。</span><span class="sxs-lookup"><span data-stu-id="10bf9-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="10bf9-116">因此，它會在作業完成後傳回結果。</span><span class="sxs-lookup"><span data-stu-id="10bf9-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="10bf9-117">此 Cmdlet 會在結果中等待1000秒。</span><span class="sxs-lookup"><span data-stu-id="10bf9-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="10bf9-118">參數</span><span class="sxs-lookup"><span data-stu-id="10bf9-118">PARAMETERS</span></span>

### <span data-ttu-id="10bf9-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="10bf9-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="10bf9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bf9-120">-DefaultProfile</span></span>
<span data-ttu-id="10bf9-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="10bf9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10bf9-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="10bf9-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="10bf9-123">指定此 Cmdlet 在放棄工作之前等待作業完成的秒數。</span><span class="sxs-lookup"><span data-stu-id="10bf9-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="10bf9-124">預設值為10800或3小時。</span><span class="sxs-lookup"><span data-stu-id="10bf9-124">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="10bf9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="10bf9-125">-Name</span></span>
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

### <span data-ttu-id="10bf9-126">-參數</span><span class="sxs-lookup"><span data-stu-id="10bf9-126">-Parameters</span></span>
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

### <span data-ttu-id="10bf9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bf9-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="10bf9-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="10bf9-128">-RunOn</span></span>
<span data-ttu-id="10bf9-129">指定要在哪個混合式輔助角色群組上執行 runbook。</span><span class="sxs-lookup"><span data-stu-id="10bf9-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="10bf9-130">-稍候</span><span class="sxs-lookup"><span data-stu-id="10bf9-130">-Wait</span></span>
<span data-ttu-id="10bf9-131">表示此 Cmdlet 會等待作業完成、暫停或失敗，然後將控制權傳回給 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="10bf9-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="10bf9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bf9-132">CommonParameters</span></span>
<span data-ttu-id="10bf9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10bf9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bf9-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10bf9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bf9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="10bf9-135">INPUTS</span></span>

### <span data-ttu-id="10bf9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="10bf9-136">System.String</span></span>

## <span data-ttu-id="10bf9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="10bf9-137">OUTPUTS</span></span>

### <span data-ttu-id="10bf9-138">[作為] 的 [自動化] 工作</span><span class="sxs-lookup"><span data-stu-id="10bf9-138">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="10bf9-139">-此 Cmdlet 會傳回 **作業** 物件，除非您指定 _Wait_ 參數。</span><span class="sxs-lookup"><span data-stu-id="10bf9-139">-This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>
<span data-ttu-id="10bf9-140">-如果您沒有指定 _Wait_ ，Azure PowerShell 會立即傳回 **作業** 物件。</span><span class="sxs-lookup"><span data-stu-id="10bf9-140">-If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="10bf9-141">-如果您指定 _Wait_ ，Azure PowerShell 完成作業，然後傳回結果。</span><span class="sxs-lookup"><span data-stu-id="10bf9-141">-If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="10bf9-142">-結果不是 **作業** 物件。</span><span class="sxs-lookup"><span data-stu-id="10bf9-142">-The result is not a **Job** object.</span></span>

### <span data-ttu-id="10bf9-143">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="10bf9-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="10bf9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="10bf9-144">NOTES</span></span>

## <span data-ttu-id="10bf9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="10bf9-145">RELATED LINKS</span></span>

[<span data-ttu-id="10bf9-146">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-147">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-148">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-149">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-150">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-151">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-152">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="10bf9-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="10bf9-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
