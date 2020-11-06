---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450329"
---
# <span data-ttu-id="2e3b8-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e3b8-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2e3b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3b8-103">建立已排程的 azure 自動化軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e3b8-104">SYNTAX</span></span>

### <span data-ttu-id="2e3b8-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="2e3b8-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e3b8-106">Linux</span><span class="sxs-lookup"><span data-stu-id="2e3b8-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e3b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="2e3b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2e3b8-108">建立在排程上執行的軟體更新設定，以更新電腦清單。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="2e3b8-109">電腦同時包含 azure 虛擬機器或非 azure 電腦。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="2e3b8-110">示例</span><span class="sxs-lookup"><span data-stu-id="2e3b8-110">EXAMPLES</span></span>

### <span data-ttu-id="2e3b8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2e3b8-111">Example 1</span></span>
<span data-ttu-id="2e3b8-112">建立軟體更新設定，以便在每星期六9PM 一次安裝兩個 Windows azure 虛擬機器上的重要更新。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="2e3b8-113">在這個範例中，[更新持續時間] 設定為 [2 小時]。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="2e3b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="2e3b8-114">PARAMETERS</span></span>

### <span data-ttu-id="2e3b8-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e3b8-115">-AutomationAccountName</span></span>
<span data-ttu-id="2e3b8-116">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-116">The automation account name.</span></span>

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

### <span data-ttu-id="2e3b8-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="2e3b8-117">-AzureVMResourceId</span></span>
<span data-ttu-id="2e3b8-118">Azure 虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="2e3b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3b8-119">-DefaultProfile</span></span>
<span data-ttu-id="2e3b8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e3b8-121">-工期</span><span class="sxs-lookup"><span data-stu-id="2e3b8-121">-Duration</span></span>
<span data-ttu-id="2e3b8-122">更新的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="2e3b8-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="2e3b8-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="2e3b8-124">已排除更新的 KB 數。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="2e3b8-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="2e3b8-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="2e3b8-126">已排除 Linux 套件遮罩。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="2e3b8-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="2e3b8-127">-IncludedKbNumber</span></span>
<span data-ttu-id="2e3b8-128">包含的更新數 KB。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="2e3b8-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="2e3b8-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="2e3b8-130">隨附的 Linux 套件分類。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="2e3b8-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="2e3b8-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="2e3b8-132">隨附的 Linux 套件遮罩。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="2e3b8-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="2e3b8-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="2e3b8-134">已包含 Windows 更新分類。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="2e3b8-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="2e3b8-135">-Linux</span></span>
<span data-ttu-id="2e3b8-136">表示軟體更新設定是以 Linux 作業系統電腦為目標。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="2e3b8-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="2e3b8-137">-NonAzureComputer</span></span>
<span data-ttu-id="2e3b8-138">非 Azure 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="2e3b8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3b8-139">-ResourceGroupName</span></span>
<span data-ttu-id="2e3b8-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-140">The resource group name.</span></span>

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

### <span data-ttu-id="2e3b8-141">-排程</span><span class="sxs-lookup"><span data-stu-id="2e3b8-141">-Schedule</span></span>
<span data-ttu-id="2e3b8-142">用於軟體更新設定的排程物件。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="2e3b8-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="2e3b8-143">-Windows</span></span>
<span data-ttu-id="2e3b8-144">表示軟體更新設定針對 windows 作業系統電腦。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="2e3b8-145">-確認</span><span class="sxs-lookup"><span data-stu-id="2e3b8-145">-Confirm</span></span>
<span data-ttu-id="2e3b8-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3b8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3b8-147">-WhatIf</span></span>
<span data-ttu-id="2e3b8-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e3b8-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3b8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3b8-150">CommonParameters</span></span>
<span data-ttu-id="2e3b8-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3b8-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3b8-153">輸入</span><span class="sxs-lookup"><span data-stu-id="2e3b8-153">INPUTS</span></span>

### <span data-ttu-id="2e3b8-154">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="2e3b8-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="2e3b8-155">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2e3b8-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2e3b8-156">System.object []</span><span class="sxs-lookup"><span data-stu-id="2e3b8-156">System.String[]</span></span>

### <span data-ttu-id="2e3b8-157">System.object</span><span class="sxs-lookup"><span data-stu-id="2e3b8-157">System.TimeSpan</span></span>

### <span data-ttu-id="2e3b8-158">WindowsUpdateClasses [] 的 UpdateManagement [命令]。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="2e3b8-159">LinuxPackageClasses [] 的 UpdateManagement [命令]。</span><span class="sxs-lookup"><span data-stu-id="2e3b8-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="2e3b8-160">System.object</span><span class="sxs-lookup"><span data-stu-id="2e3b8-160">System.String</span></span>

## <span data-ttu-id="2e3b8-161">輸出</span><span class="sxs-lookup"><span data-stu-id="2e3b8-161">OUTPUTS</span></span>

### <span data-ttu-id="2e3b8-162">UpdateManagement SoftwareUpdateConfiguration 中的 []</span><span class="sxs-lookup"><span data-stu-id="2e3b8-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2e3b8-163">筆記</span><span class="sxs-lookup"><span data-stu-id="2e3b8-163">NOTES</span></span>

## <span data-ttu-id="2e3b8-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e3b8-164">RELATED LINKS</span></span>
