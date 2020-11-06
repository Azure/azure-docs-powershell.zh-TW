---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452608"
---
# <span data-ttu-id="0c0f8-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="0c0f8-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="0c0f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0f8-103">在自動化中取得 DSC 編譯作業。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c0f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c0f8-104">SYNTAX</span></span>

### <span data-ttu-id="0c0f8-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="0c0f8-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c0f8-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="0c0f8-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c0f8-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0c0f8-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c0f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="0c0f8-108">DESCRIPTION</span></span>
<span data-ttu-id="0c0f8-109">**AzureRmAutomationDscCompilationJob** Cmdlet 會在 Azure 自動化中取得 DSC) 編譯作業 (的 Ap 所需狀態設定。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="0c0f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="0c0f8-110">EXAMPLES</span></span>

### <span data-ttu-id="0c0f8-111">範例1：取得所有的 DSC 編譯作業</span><span class="sxs-lookup"><span data-stu-id="0c0f8-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0c0f8-112">這個命令會取得自動帳戶（名為 Contoso17）中的所有編譯作業。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0c0f8-113">範例2：取得設定的 DSC 編譯作業</span><span class="sxs-lookup"><span data-stu-id="0c0f8-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="0c0f8-114">這個命令會針對自動化帳戶（名為 Contoso17）中名為 ContosoConfiguration 的 DSC 配置取得所有編譯作業。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0c0f8-115">範例3：取得特定的 DSC 編譯作業</span><span class="sxs-lookup"><span data-stu-id="0c0f8-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="0c0f8-116">這個命令會取得自動化帳戶（名為 Contoso17）中具有指定識別碼的編譯作業。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0c0f8-117">參數</span><span class="sxs-lookup"><span data-stu-id="0c0f8-117">PARAMETERS</span></span>

### <span data-ttu-id="0c0f8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c0f8-118">-AutomationAccountName</span></span>
<span data-ttu-id="0c0f8-119">指定包含此 Cmdlet 所取得的 DSC 編譯作業之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c0f8-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0c0f8-120">-ConfigurationName</span></span>
<span data-ttu-id="0c0f8-121">指定此 Cmdlet 取得編譯作業的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="0c0f8-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0c0f8-122">-EndTime</span></span>
<span data-ttu-id="0c0f8-123">指定結束時間。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-123">Specifies an end time.</span></span>
<span data-ttu-id="0c0f8-124">這個 Cmdlet 會取得已在此參數指定時間開始的編譯作業。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c0f8-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0c0f8-125">-Id</span></span>
<span data-ttu-id="0c0f8-126">指定此 Cmdlet 取得之 DSC 編譯作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c0f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c0f8-127">-ResourceGroupName</span></span>
<span data-ttu-id="0c0f8-128">指定此 Cmdlet 取得 DSC 編譯作業之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="0c0f8-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0c0f8-129">-StartTime</span></span>
<span data-ttu-id="0c0f8-130">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-130">Specifies a start time.</span></span>
<span data-ttu-id="0c0f8-131">這個 Cmdlet 會取得在此參數指定時間之後或之後開始的作業。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c0f8-132">-狀態</span><span class="sxs-lookup"><span data-stu-id="0c0f8-132">-Status</span></span>
<span data-ttu-id="0c0f8-133">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0c0f8-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="0c0f8-134">Valid values are:</span></span> 

- <span data-ttu-id="0c0f8-135">完畢</span><span class="sxs-lookup"><span data-stu-id="0c0f8-135">Completed</span></span> 
- <span data-ttu-id="0c0f8-136">成功</span><span class="sxs-lookup"><span data-stu-id="0c0f8-136">Failed</span></span> 
- <span data-ttu-id="0c0f8-137">排</span><span class="sxs-lookup"><span data-stu-id="0c0f8-137">Queued</span></span> 
- <span data-ttu-id="0c0f8-138">入門</span><span class="sxs-lookup"><span data-stu-id="0c0f8-138">Starting</span></span> 
- <span data-ttu-id="0c0f8-139">開始</span><span class="sxs-lookup"><span data-stu-id="0c0f8-139">Resuming</span></span> 
- <span data-ttu-id="0c0f8-140">進行</span><span class="sxs-lookup"><span data-stu-id="0c0f8-140">Running</span></span> 
- <span data-ttu-id="0c0f8-141">被</span><span class="sxs-lookup"><span data-stu-id="0c0f8-141">Stopped</span></span> 
- <span data-ttu-id="0c0f8-142">終止</span><span class="sxs-lookup"><span data-stu-id="0c0f8-142">Stopping</span></span> 
- <span data-ttu-id="0c0f8-143">封存</span><span class="sxs-lookup"><span data-stu-id="0c0f8-143">Suspended</span></span> 
- <span data-ttu-id="0c0f8-144">封存</span><span class="sxs-lookup"><span data-stu-id="0c0f8-144">Suspending</span></span> 
- <span data-ttu-id="0c0f8-145">啟用</span><span class="sxs-lookup"><span data-stu-id="0c0f8-145">Activating</span></span>
- <span data-ttu-id="0c0f8-146">新增功能</span><span class="sxs-lookup"><span data-stu-id="0c0f8-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0f8-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0f8-147">-DefaultProfile</span></span>
<span data-ttu-id="0c0f8-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c0f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0f8-149">CommonParameters</span></span>
<span data-ttu-id="0c0f8-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0f8-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c0f8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0f8-152">輸入</span><span class="sxs-lookup"><span data-stu-id="0c0f8-152">INPUTS</span></span>

## <span data-ttu-id="0c0f8-153">輸出</span><span class="sxs-lookup"><span data-stu-id="0c0f8-153">OUTPUTS</span></span>

### <span data-ttu-id="0c0f8-154">CompilationJob 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c0f8-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="0c0f8-155">筆記</span><span class="sxs-lookup"><span data-stu-id="0c0f8-155">NOTES</span></span>

## <span data-ttu-id="0c0f8-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c0f8-156">RELATED LINKS</span></span>

[<span data-ttu-id="0c0f8-157">AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0c0f8-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="0c0f8-158">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="0c0f8-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


