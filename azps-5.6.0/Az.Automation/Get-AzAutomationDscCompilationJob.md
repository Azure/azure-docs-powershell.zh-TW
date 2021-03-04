---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5157b4d4e1a291193f10fef22308002de210e748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912494"
---
# <span data-ttu-id="9420c-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9420c-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="9420c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9420c-102">SYNOPSIS</span></span>
<span data-ttu-id="9420c-103">在自動化中獲得 DSC 編譯工作。</span><span class="sxs-lookup"><span data-stu-id="9420c-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="9420c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9420c-104">SYNTAX</span></span>

### <span data-ttu-id="9420c-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="9420c-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9420c-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="9420c-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9420c-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9420c-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9420c-108">描述</span><span class="sxs-lookup"><span data-stu-id="9420c-108">DESCRIPTION</span></span>
<span data-ttu-id="9420c-109">**Get-AzAutomationDscCompilationJob** Cmdlet 會取得 Azure Automation 中的 APS (DSC) 編譯工作。</span><span class="sxs-lookup"><span data-stu-id="9420c-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="9420c-110">例子</span><span class="sxs-lookup"><span data-stu-id="9420c-110">EXAMPLES</span></span>

### <span data-ttu-id="9420c-111">範例 1：取得所有 DSC 編譯工作</span><span class="sxs-lookup"><span data-stu-id="9420c-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9420c-112">此命令會獲得自動化帳戶中名為 Contoso17 的所有編譯工作。</span><span class="sxs-lookup"><span data-stu-id="9420c-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9420c-113">範例 2：取得組配置的 DSC 編譯工作</span><span class="sxs-lookup"><span data-stu-id="9420c-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="9420c-114">此命令會針對名為 Contoso17 的自動化帳戶中名為 ContosoConfiguration 的 DSC 組式，獲得所有編譯工作。</span><span class="sxs-lookup"><span data-stu-id="9420c-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9420c-115">範例 3：取得特定的 DSC 編譯工作</span><span class="sxs-lookup"><span data-stu-id="9420c-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="9420c-116">此命令會使用自動化帳戶中指定識別碼的編譯工作，名稱為 Contoso17。</span><span class="sxs-lookup"><span data-stu-id="9420c-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9420c-117">參數</span><span class="sxs-lookup"><span data-stu-id="9420c-117">PARAMETERS</span></span>

### <span data-ttu-id="9420c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9420c-118">-AutomationAccountName</span></span>
<span data-ttu-id="9420c-119">指定包含此 Cmdlet 所獲取之 DSC 編譯工作的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9420c-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9420c-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9420c-120">-ConfigurationName</span></span>
<span data-ttu-id="9420c-121">指定此 Cmdlet 可進行編譯工作的 DSC 組名。</span><span class="sxs-lookup"><span data-stu-id="9420c-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9420c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9420c-122">-DefaultProfile</span></span>
<span data-ttu-id="9420c-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9420c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9420c-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9420c-124">-EndTime</span></span>
<span data-ttu-id="9420c-125">指定結束時間。</span><span class="sxs-lookup"><span data-stu-id="9420c-125">Specifies an end time.</span></span>
<span data-ttu-id="9420c-126">此 Cmdlet 會獲得開始到此參數指定之時間之編譯工作。</span><span class="sxs-lookup"><span data-stu-id="9420c-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9420c-127">-Id</span><span class="sxs-lookup"><span data-stu-id="9420c-127">-Id</span></span>
<span data-ttu-id="9420c-128">指定此 Cmdlet 所獲得 DSC 編譯工作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9420c-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9420c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9420c-129">-ResourceGroupName</span></span>
<span data-ttu-id="9420c-130">指定此 Cmdlet 會在此資源群組中獲得 DSC 編譯工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="9420c-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="9420c-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9420c-131">-StartTime</span></span>
<span data-ttu-id="9420c-132">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="9420c-132">Specifies a start time.</span></span>
<span data-ttu-id="9420c-133">此 Cmdlet 會獲得在此參數指定之時間開始或之後的工作。</span><span class="sxs-lookup"><span data-stu-id="9420c-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9420c-134">-狀態</span><span class="sxs-lookup"><span data-stu-id="9420c-134">-Status</span></span>
<span data-ttu-id="9420c-135">指定此 Cmdlet 獲得的工作狀態。</span><span class="sxs-lookup"><span data-stu-id="9420c-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9420c-136">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="9420c-136">Valid values are:</span></span> 
- <span data-ttu-id="9420c-137">完成</span><span class="sxs-lookup"><span data-stu-id="9420c-137">Completed</span></span> 
- <span data-ttu-id="9420c-138">失敗</span><span class="sxs-lookup"><span data-stu-id="9420c-138">Failed</span></span> 
- <span data-ttu-id="9420c-139">排隊</span><span class="sxs-lookup"><span data-stu-id="9420c-139">Queued</span></span> 
- <span data-ttu-id="9420c-140">開始</span><span class="sxs-lookup"><span data-stu-id="9420c-140">Starting</span></span> 
- <span data-ttu-id="9420c-141">恢復</span><span class="sxs-lookup"><span data-stu-id="9420c-141">Resuming</span></span> 
- <span data-ttu-id="9420c-142">運行</span><span class="sxs-lookup"><span data-stu-id="9420c-142">Running</span></span> 
- <span data-ttu-id="9420c-143">停止</span><span class="sxs-lookup"><span data-stu-id="9420c-143">Stopped</span></span> 
- <span data-ttu-id="9420c-144">停止</span><span class="sxs-lookup"><span data-stu-id="9420c-144">Stopping</span></span> 
- <span data-ttu-id="9420c-145">暫停</span><span class="sxs-lookup"><span data-stu-id="9420c-145">Suspended</span></span> 
- <span data-ttu-id="9420c-146">暫停</span><span class="sxs-lookup"><span data-stu-id="9420c-146">Suspending</span></span> 
- <span data-ttu-id="9420c-147">啟動</span><span class="sxs-lookup"><span data-stu-id="9420c-147">Activating</span></span>
- <span data-ttu-id="9420c-148">新增功能</span><span class="sxs-lookup"><span data-stu-id="9420c-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9420c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9420c-149">CommonParameters</span></span>
<span data-ttu-id="9420c-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9420c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9420c-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9420c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9420c-152">輸入</span><span class="sxs-lookup"><span data-stu-id="9420c-152">INPUTS</span></span>

### <span data-ttu-id="9420c-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9420c-153">System.Guid</span></span>

### <span data-ttu-id="9420c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="9420c-154">System.String</span></span>

## <span data-ttu-id="9420c-155">輸出</span><span class="sxs-lookup"><span data-stu-id="9420c-155">OUTPUTS</span></span>

### <span data-ttu-id="9420c-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="9420c-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="9420c-157">筆記</span><span class="sxs-lookup"><span data-stu-id="9420c-157">NOTES</span></span>

## <span data-ttu-id="9420c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="9420c-158">RELATED LINKS</span></span>

[<span data-ttu-id="9420c-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9420c-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="9420c-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9420c-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


