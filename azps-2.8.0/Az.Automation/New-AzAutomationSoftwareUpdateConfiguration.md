---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f441df5be99764f9582939d4c4d5d422ea88c97f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613737"
---
# <span data-ttu-id="30b80-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="30b80-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="30b80-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30b80-102">SYNOPSIS</span></span>
<span data-ttu-id="30b80-103">建立已排程的 azure 自動化軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="30b80-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="30b80-104">句法</span><span class="sxs-lookup"><span data-stu-id="30b80-104">SYNTAX</span></span>

### <span data-ttu-id="30b80-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="30b80-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30b80-106">Linux</span><span class="sxs-lookup"><span data-stu-id="30b80-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30b80-107">說明</span><span class="sxs-lookup"><span data-stu-id="30b80-107">DESCRIPTION</span></span>
<span data-ttu-id="30b80-108">建立在排程上執行的軟體更新設定，以更新電腦清單。</span><span class="sxs-lookup"><span data-stu-id="30b80-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="30b80-109">電腦同時包含 azure 虛擬機器或非 az 電腦。</span><span class="sxs-lookup"><span data-stu-id="30b80-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="30b80-110">示例</span><span class="sxs-lookup"><span data-stu-id="30b80-110">EXAMPLES</span></span>

### <span data-ttu-id="30b80-111">範例1</span><span class="sxs-lookup"><span data-stu-id="30b80-111">Example 1</span></span>
<span data-ttu-id="30b80-112">建立軟體更新設定，以便在每星期六9PM 一次安裝兩個 Windows azure 虛擬機器上的重要更新。</span><span class="sxs-lookup"><span data-stu-id="30b80-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="30b80-113">在這個範例中，[更新持續時間] 設定為 [2 小時]。</span><span class="sxs-lookup"><span data-stu-id="30b80-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="30b80-114">參數</span><span class="sxs-lookup"><span data-stu-id="30b80-114">PARAMETERS</span></span>

### <span data-ttu-id="30b80-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30b80-115">-AutomationAccountName</span></span>
<span data-ttu-id="30b80-116">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="30b80-116">The automation account name.</span></span>

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

### <span data-ttu-id="30b80-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="30b80-117">-AzureQuery</span></span>
<span data-ttu-id="30b80-118">動態群組 azure 查詢。</span><span class="sxs-lookup"><span data-stu-id="30b80-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="30b80-119">-AzureVMResourceId</span></span>
<span data-ttu-id="30b80-120">Azure 虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30b80-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b80-121">-DefaultProfile</span></span>
<span data-ttu-id="30b80-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30b80-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-123">-工期</span><span class="sxs-lookup"><span data-stu-id="30b80-123">-Duration</span></span>
<span data-ttu-id="30b80-124">更新的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="30b80-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="30b80-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="30b80-126">已排除更新的 KB 數。</span><span class="sxs-lookup"><span data-stu-id="30b80-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="30b80-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="30b80-128">已排除 Linux 套件遮罩。</span><span class="sxs-lookup"><span data-stu-id="30b80-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="30b80-129">-IncludedKbNumber</span></span>
<span data-ttu-id="30b80-130">包含的更新數 KB。</span><span class="sxs-lookup"><span data-stu-id="30b80-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="30b80-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="30b80-132">隨附的 Linux 套件分類。</span><span class="sxs-lookup"><span data-stu-id="30b80-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="30b80-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="30b80-134">隨附的 Linux 套件遮罩。</span><span class="sxs-lookup"><span data-stu-id="30b80-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="30b80-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="30b80-136">已包含 Windows 更新分類。</span><span class="sxs-lookup"><span data-stu-id="30b80-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="30b80-137">-Linux</span></span>
<span data-ttu-id="30b80-138">表示軟體更新設定是以 Linux 作業系統電腦為目標。</span><span class="sxs-lookup"><span data-stu-id="30b80-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="30b80-139">-NonAzureComputer</span></span>
<span data-ttu-id="30b80-140">非 Az 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="30b80-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="30b80-141">-NonAzureQuery</span></span>
<span data-ttu-id="30b80-142">動態群組非 Azure 查詢。</span><span class="sxs-lookup"><span data-stu-id="30b80-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="30b80-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="30b80-144">[張貼工作]。</span><span class="sxs-lookup"><span data-stu-id="30b80-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="30b80-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="30b80-146">[張貼任務] 參數。</span><span class="sxs-lookup"><span data-stu-id="30b80-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="30b80-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="30b80-148">前置任務。</span><span class="sxs-lookup"><span data-stu-id="30b80-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="30b80-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="30b80-150">前置任務參數。</span><span class="sxs-lookup"><span data-stu-id="30b80-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="30b80-151">-RebootOnly</span></span>
<span data-ttu-id="30b80-152">表示軟體更新設定將只會重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="30b80-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="30b80-153">-RebootSetting</span></span>
<span data-ttu-id="30b80-154">重新開機設定。</span><span class="sxs-lookup"><span data-stu-id="30b80-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b80-155">-ResourceGroupName</span></span>
<span data-ttu-id="30b80-156">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30b80-156">The resource group name.</span></span>

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

### <span data-ttu-id="30b80-157">-排程</span><span class="sxs-lookup"><span data-stu-id="30b80-157">-Schedule</span></span>
<span data-ttu-id="30b80-158">用於軟體更新設定的排程物件。</span><span class="sxs-lookup"><span data-stu-id="30b80-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="30b80-159">-Windows</span></span>
<span data-ttu-id="30b80-160">表示軟體更新設定針對 windows 作業系統電腦。</span><span class="sxs-lookup"><span data-stu-id="30b80-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-161">-確認</span><span class="sxs-lookup"><span data-stu-id="30b80-161">-Confirm</span></span>
<span data-ttu-id="30b80-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30b80-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30b80-163">-WhatIf</span></span>
<span data-ttu-id="30b80-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30b80-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30b80-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30b80-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b80-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b80-166">CommonParameters</span></span>
<span data-ttu-id="30b80-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30b80-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b80-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30b80-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b80-169">輸入</span><span class="sxs-lookup"><span data-stu-id="30b80-169">INPUTS</span></span>

### <span data-ttu-id="30b80-170">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="30b80-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="30b80-171">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="30b80-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="30b80-172">System.object []</span><span class="sxs-lookup"><span data-stu-id="30b80-172">System.String[]</span></span>

### <span data-ttu-id="30b80-173">System.object</span><span class="sxs-lookup"><span data-stu-id="30b80-173">System.TimeSpan</span></span>

### <span data-ttu-id="30b80-174">WindowsUpdateClasses [] 的 UpdateManagement [命令]。</span><span class="sxs-lookup"><span data-stu-id="30b80-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="30b80-175">LinuxPackageClasses [] 的 UpdateManagement [命令]。</span><span class="sxs-lookup"><span data-stu-id="30b80-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="30b80-176">System.object</span><span class="sxs-lookup"><span data-stu-id="30b80-176">System.String</span></span>

## <span data-ttu-id="30b80-177">輸出</span><span class="sxs-lookup"><span data-stu-id="30b80-177">OUTPUTS</span></span>

### <span data-ttu-id="30b80-178">UpdateManagement SoftwareUpdateConfiguration 中的 []</span><span class="sxs-lookup"><span data-stu-id="30b80-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="30b80-179">筆記</span><span class="sxs-lookup"><span data-stu-id="30b80-179">NOTES</span></span>

## <span data-ttu-id="30b80-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="30b80-180">RELATED LINKS</span></span>
