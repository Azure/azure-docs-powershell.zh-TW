---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970666"
---
# <span data-ttu-id="96c17-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="96c17-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="96c17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96c17-102">SYNOPSIS</span></span>
<span data-ttu-id="96c17-103">在自動化中取得 DSC 編譯作業。</span><span class="sxs-lookup"><span data-stu-id="96c17-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="96c17-104">句法</span><span class="sxs-lookup"><span data-stu-id="96c17-104">SYNTAX</span></span>

### <span data-ttu-id="96c17-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="96c17-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96c17-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="96c17-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c17-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="96c17-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c17-108">說明</span><span class="sxs-lookup"><span data-stu-id="96c17-108">DESCRIPTION</span></span>
<span data-ttu-id="96c17-109">**AzAutomationDscCompilationJob** Cmdlet 會在 Azure 自動化中取得 DSC) 編譯作業 (的 Ap 所需狀態設定。</span><span class="sxs-lookup"><span data-stu-id="96c17-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="96c17-110">示例</span><span class="sxs-lookup"><span data-stu-id="96c17-110">EXAMPLES</span></span>

### <span data-ttu-id="96c17-111">範例1：取得所有的 DSC 編譯作業</span><span class="sxs-lookup"><span data-stu-id="96c17-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="96c17-112">這個命令會取得自動帳戶（名為 Contoso17）中的所有編譯作業。</span><span class="sxs-lookup"><span data-stu-id="96c17-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="96c17-113">範例2：取得設定的 DSC 編譯作業</span><span class="sxs-lookup"><span data-stu-id="96c17-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="96c17-114">這個命令會針對自動化帳戶（名為 Contoso17）中名為 ContosoConfiguration 的 DSC 配置取得所有編譯作業。</span><span class="sxs-lookup"><span data-stu-id="96c17-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="96c17-115">範例3：取得特定的 DSC 編譯作業</span><span class="sxs-lookup"><span data-stu-id="96c17-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="96c17-116">這個命令會取得自動化帳戶（名為 Contoso17）中具有指定識別碼的編譯作業。</span><span class="sxs-lookup"><span data-stu-id="96c17-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="96c17-117">參數</span><span class="sxs-lookup"><span data-stu-id="96c17-117">PARAMETERS</span></span>

### <span data-ttu-id="96c17-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96c17-118">-AutomationAccountName</span></span>
<span data-ttu-id="96c17-119">指定包含此 Cmdlet 所取得的 DSC 編譯作業之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="96c17-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="96c17-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="96c17-120">-ConfigurationName</span></span>
<span data-ttu-id="96c17-121">指定此 Cmdlet 取得編譯作業的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="96c17-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="96c17-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c17-122">-DefaultProfile</span></span>
<span data-ttu-id="96c17-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="96c17-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96c17-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="96c17-124">-EndTime</span></span>
<span data-ttu-id="96c17-125">指定結束時間。</span><span class="sxs-lookup"><span data-stu-id="96c17-125">Specifies an end time.</span></span>
<span data-ttu-id="96c17-126">這個 Cmdlet 會取得已在此參數指定時間開始的編譯作業。</span><span class="sxs-lookup"><span data-stu-id="96c17-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="96c17-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="96c17-127">-Id</span></span>
<span data-ttu-id="96c17-128">指定此 Cmdlet 取得之 DSC 編譯作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="96c17-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="96c17-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c17-129">-ResourceGroupName</span></span>
<span data-ttu-id="96c17-130">指定此 Cmdlet 取得 DSC 編譯作業之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96c17-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="96c17-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="96c17-131">-StartTime</span></span>
<span data-ttu-id="96c17-132">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="96c17-132">Specifies a start time.</span></span>
<span data-ttu-id="96c17-133">這個 Cmdlet 會取得在此參數指定時間之後或之後開始的作業。</span><span class="sxs-lookup"><span data-stu-id="96c17-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="96c17-134">-狀態</span><span class="sxs-lookup"><span data-stu-id="96c17-134">-Status</span></span>
<span data-ttu-id="96c17-135">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="96c17-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="96c17-136">有效值為：</span><span class="sxs-lookup"><span data-stu-id="96c17-136">Valid values are:</span></span> 
- <span data-ttu-id="96c17-137">完畢</span><span class="sxs-lookup"><span data-stu-id="96c17-137">Completed</span></span> 
- <span data-ttu-id="96c17-138">成功</span><span class="sxs-lookup"><span data-stu-id="96c17-138">Failed</span></span> 
- <span data-ttu-id="96c17-139">排</span><span class="sxs-lookup"><span data-stu-id="96c17-139">Queued</span></span> 
- <span data-ttu-id="96c17-140">入門</span><span class="sxs-lookup"><span data-stu-id="96c17-140">Starting</span></span> 
- <span data-ttu-id="96c17-141">開始</span><span class="sxs-lookup"><span data-stu-id="96c17-141">Resuming</span></span> 
- <span data-ttu-id="96c17-142">進行</span><span class="sxs-lookup"><span data-stu-id="96c17-142">Running</span></span> 
- <span data-ttu-id="96c17-143">被</span><span class="sxs-lookup"><span data-stu-id="96c17-143">Stopped</span></span> 
- <span data-ttu-id="96c17-144">終止</span><span class="sxs-lookup"><span data-stu-id="96c17-144">Stopping</span></span> 
- <span data-ttu-id="96c17-145">封存</span><span class="sxs-lookup"><span data-stu-id="96c17-145">Suspended</span></span> 
- <span data-ttu-id="96c17-146">封存</span><span class="sxs-lookup"><span data-stu-id="96c17-146">Suspending</span></span> 
- <span data-ttu-id="96c17-147">啟用</span><span class="sxs-lookup"><span data-stu-id="96c17-147">Activating</span></span>
- <span data-ttu-id="96c17-148">新增功能</span><span class="sxs-lookup"><span data-stu-id="96c17-148">New</span></span>

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

### <span data-ttu-id="96c17-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c17-149">CommonParameters</span></span>
<span data-ttu-id="96c17-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96c17-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c17-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96c17-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c17-152">輸入</span><span class="sxs-lookup"><span data-stu-id="96c17-152">INPUTS</span></span>

### <span data-ttu-id="96c17-153">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="96c17-153">System.Guid</span></span>

### <span data-ttu-id="96c17-154">System.object</span><span class="sxs-lookup"><span data-stu-id="96c17-154">System.String</span></span>

## <span data-ttu-id="96c17-155">輸出</span><span class="sxs-lookup"><span data-stu-id="96c17-155">OUTPUTS</span></span>

### <span data-ttu-id="96c17-156">CompilationJob 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96c17-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="96c17-157">筆記</span><span class="sxs-lookup"><span data-stu-id="96c17-157">NOTES</span></span>

## <span data-ttu-id="96c17-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="96c17-158">RELATED LINKS</span></span>

[<span data-ttu-id="96c17-159">AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="96c17-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="96c17-160">開始-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="96c17-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


