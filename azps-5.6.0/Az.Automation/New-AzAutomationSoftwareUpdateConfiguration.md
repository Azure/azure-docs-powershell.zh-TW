---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 4b62b04b0b394c590cd04ab30201575bb98d90b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902149"
---
# <span data-ttu-id="bd312-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd312-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="bd312-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd312-102">SYNOPSIS</span></span>
<span data-ttu-id="bd312-103">建立已排程的 Azure 自動化軟體更新組程。</span><span class="sxs-lookup"><span data-stu-id="bd312-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="bd312-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd312-104">SYNTAX</span></span>

### <span data-ttu-id="bd312-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="bd312-105">Windows (Default)</span></span>
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

### <span data-ttu-id="bd312-106">Linux</span><span class="sxs-lookup"><span data-stu-id="bd312-106">Linux</span></span>
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

## <span data-ttu-id="bd312-107">描述</span><span class="sxs-lookup"><span data-stu-id="bd312-107">DESCRIPTION</span></span>
<span data-ttu-id="bd312-108">建立可排程執行的更新軟體更新組式，以更新電腦清單。</span><span class="sxs-lookup"><span data-stu-id="bd312-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="bd312-109">電腦包括 Azure 虛擬機器或非 az 電腦。</span><span class="sxs-lookup"><span data-stu-id="bd312-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="bd312-110">例子</span><span class="sxs-lookup"><span data-stu-id="bd312-110">EXAMPLES</span></span>

### <span data-ttu-id="bd312-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bd312-111">Example 1</span></span>
<span data-ttu-id="bd312-112">建立軟體更新組式，以每週六晚上 9 點在兩部 Windows Azure 虛擬機器上安裝一次重大更新。</span><span class="sxs-lookup"><span data-stu-id="bd312-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="bd312-113">在此範例中，更新持續時間設定為 2 小時。</span><span class="sxs-lookup"><span data-stu-id="bd312-113">Update duration is set to 2 hours in this example.</span></span>

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
                                                 -AzureVMResourceId $targetMachines `
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

## <span data-ttu-id="bd312-114">參數</span><span class="sxs-lookup"><span data-stu-id="bd312-114">PARAMETERS</span></span>

### <span data-ttu-id="bd312-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bd312-115">-AutomationAccountName</span></span>
<span data-ttu-id="bd312-116">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bd312-116">The automation account name.</span></span>

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

### <span data-ttu-id="bd312-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="bd312-117">-AzureQuery</span></span>
<span data-ttu-id="bd312-118">動態群組 azure 查詢。</span><span class="sxs-lookup"><span data-stu-id="bd312-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="bd312-119">-AzureEVResourceId</span><span class="sxs-lookup"><span data-stu-id="bd312-119">-AzureVMResourceId</span></span>
<span data-ttu-id="bd312-120">Azure 虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd312-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="bd312-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd312-121">-DefaultProfile</span></span>
<span data-ttu-id="bd312-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd312-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd312-123">-工期</span><span class="sxs-lookup"><span data-stu-id="bd312-123">-Duration</span></span>
<span data-ttu-id="bd312-124">更新的持續時間上限。</span><span class="sxs-lookup"><span data-stu-id="bd312-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="bd312-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="bd312-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="bd312-126">排除更新的 KB 數目。</span><span class="sxs-lookup"><span data-stu-id="bd312-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="bd312-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="bd312-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="bd312-128">排除的 Linux 封裝遮罩。</span><span class="sxs-lookup"><span data-stu-id="bd312-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="bd312-129">-包含KbNumber</span><span class="sxs-lookup"><span data-stu-id="bd312-129">-IncludedKbNumber</span></span>
<span data-ttu-id="bd312-130">包含更新的 KB 編號。</span><span class="sxs-lookup"><span data-stu-id="bd312-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="bd312-131">-包含PackageClassification</span><span class="sxs-lookup"><span data-stu-id="bd312-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="bd312-132">包含 Linux 套件分類。</span><span class="sxs-lookup"><span data-stu-id="bd312-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="bd312-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="bd312-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="bd312-134">包含的 Linux 封裝遮罩。</span><span class="sxs-lookup"><span data-stu-id="bd312-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="bd312-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="bd312-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="bd312-136">包含的 Windows Update 分類。</span><span class="sxs-lookup"><span data-stu-id="bd312-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="bd312-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="bd312-137">-Linux</span></span>
<span data-ttu-id="bd312-138">表示軟體更新組配置的目標為 Linux 作業系統電腦。</span><span class="sxs-lookup"><span data-stu-id="bd312-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="bd312-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="bd312-139">-NonAzureComputer</span></span>
<span data-ttu-id="bd312-140">非 Az 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="bd312-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="bd312-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="bd312-141">-NonAzureQuery</span></span>
<span data-ttu-id="bd312-142">動態群組非 Azure 查詢。</span><span class="sxs-lookup"><span data-stu-id="bd312-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="bd312-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="bd312-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="bd312-144">張貼工作。</span><span class="sxs-lookup"><span data-stu-id="bd312-144">Post task.</span></span>

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

### <span data-ttu-id="bd312-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="bd312-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="bd312-146">張貼任務參數。</span><span class="sxs-lookup"><span data-stu-id="bd312-146">Post task parameter.</span></span>

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

### <span data-ttu-id="bd312-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="bd312-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="bd312-148">工作前。</span><span class="sxs-lookup"><span data-stu-id="bd312-148">Pre task.</span></span>

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

### <span data-ttu-id="bd312-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="bd312-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="bd312-150">預先任務參數。</span><span class="sxs-lookup"><span data-stu-id="bd312-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="bd312-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="bd312-151">-RebootOnly</span></span>
<span data-ttu-id="bd312-152">表示軟體更新組式只會重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="bd312-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="bd312-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="bd312-153">-RebootSetting</span></span>
<span data-ttu-id="bd312-154">重新開機設定。</span><span class="sxs-lookup"><span data-stu-id="bd312-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="bd312-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd312-155">-ResourceGroupName</span></span>
<span data-ttu-id="bd312-156">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bd312-156">The resource group name.</span></span>

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

### <span data-ttu-id="bd312-157">-排程</span><span class="sxs-lookup"><span data-stu-id="bd312-157">-Schedule</span></span>
<span data-ttu-id="bd312-158">用於軟體更新配置的排程物件。</span><span class="sxs-lookup"><span data-stu-id="bd312-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="bd312-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="bd312-159">-Windows</span></span>
<span data-ttu-id="bd312-160">表示軟體更新組配置的目標為 Windows 作業系統電腦。</span><span class="sxs-lookup"><span data-stu-id="bd312-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="bd312-161">-確認</span><span class="sxs-lookup"><span data-stu-id="bd312-161">-Confirm</span></span>
<span data-ttu-id="bd312-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bd312-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd312-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd312-163">-WhatIf</span></span>
<span data-ttu-id="bd312-164">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd312-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd312-165">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd312-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd312-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd312-166">CommonParameters</span></span>
<span data-ttu-id="bd312-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd312-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd312-168">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bd312-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd312-169">輸入</span><span class="sxs-lookup"><span data-stu-id="bd312-169">INPUTS</span></span>

### <span data-ttu-id="bd312-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="bd312-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="bd312-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd312-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bd312-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bd312-172">System.String[]</span></span>

### <span data-ttu-id="bd312-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="bd312-173">System.TimeSpan</span></span>

### <span data-ttu-id="bd312-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="bd312-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="bd312-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="bd312-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="bd312-176">System.String</span><span class="sxs-lookup"><span data-stu-id="bd312-176">System.String</span></span>

## <span data-ttu-id="bd312-177">輸出</span><span class="sxs-lookup"><span data-stu-id="bd312-177">OUTPUTS</span></span>

### <span data-ttu-id="bd312-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd312-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="bd312-179">筆記</span><span class="sxs-lookup"><span data-stu-id="bd312-179">NOTES</span></span>

## <span data-ttu-id="bd312-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd312-180">RELATED LINKS</span></span>
