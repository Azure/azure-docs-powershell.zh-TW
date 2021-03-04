---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: 49c8693984dc695f3d47b8066228cf2f82d5b267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917465"
---
# <span data-ttu-id="07715-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="07715-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="07715-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07715-102">SYNOPSIS</span></span>
<span data-ttu-id="07715-103">獲得 Azure 自動化軟體更新執行的清單。</span><span class="sxs-lookup"><span data-stu-id="07715-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="07715-104">語法</span><span class="sxs-lookup"><span data-stu-id="07715-104">SYNTAX</span></span>

### <span data-ttu-id="07715-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="07715-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07715-106">ById</span><span class="sxs-lookup"><span data-stu-id="07715-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07715-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="07715-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07715-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="07715-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07715-109">描述</span><span class="sxs-lookup"><span data-stu-id="07715-109">DESCRIPTION</span></span>
<span data-ttu-id="07715-110">Cmdlet Get-AzAutomationSoftwareUpdateRun會執行軟體更新清單。</span><span class="sxs-lookup"><span data-stu-id="07715-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="07715-111">由於軟體更新組程具有相關聯的排程，因此可以觸發多次。</span><span class="sxs-lookup"><span data-stu-id="07715-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="07715-112">每次觸發排程時，都會建立更新執行。</span><span class="sxs-lookup"><span data-stu-id="07715-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="07715-113">更新執行是所有電腦執行結果的匯總。</span><span class="sxs-lookup"><span data-stu-id="07715-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="07715-114">您可以傳遞 SoftwareUpdateConfigurationName 參數，以執行特定軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="07715-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="07715-115">若要執行特定作業，您必須傳遞名稱參數。</span><span class="sxs-lookup"><span data-stu-id="07715-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="07715-116">您也可以以特定狀態列出執行、執行目標特定作業系統，或傳遞適當參數，于特定時間之後開始執行。</span><span class="sxs-lookup"><span data-stu-id="07715-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="07715-117">例子</span><span class="sxs-lookup"><span data-stu-id="07715-117">EXAMPLES</span></span>

### <span data-ttu-id="07715-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="07715-118">Example 1</span></span>
<span data-ttu-id="07715-119">此範例清單會執行由特定軟體更新組配置觸發的所有更新。</span><span class="sxs-lookup"><span data-stu-id="07715-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="07715-120">參數</span><span class="sxs-lookup"><span data-stu-id="07715-120">PARAMETERS</span></span>

### <span data-ttu-id="07715-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="07715-121">-AutomationAccountName</span></span>
<span data-ttu-id="07715-122">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="07715-122">The automation account name.</span></span>

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

### <span data-ttu-id="07715-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07715-123">-DefaultProfile</span></span>
<span data-ttu-id="07715-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07715-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07715-125">-Id</span><span class="sxs-lookup"><span data-stu-id="07715-125">-Id</span></span>
<span data-ttu-id="07715-126">執行軟體更新配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="07715-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07715-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="07715-127">-OperatingSystem</span></span>
<span data-ttu-id="07715-128">執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="07715-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07715-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07715-129">-ResourceGroupName</span></span>
<span data-ttu-id="07715-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="07715-130">The resource group name.</span></span>

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

### <span data-ttu-id="07715-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="07715-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="07715-132">軟體更新組會觸發執行。</span><span class="sxs-lookup"><span data-stu-id="07715-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07715-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="07715-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="07715-134">軟體更新組組的名稱已觸發執行。</span><span class="sxs-lookup"><span data-stu-id="07715-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07715-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="07715-135">-StartTime</span></span>
<span data-ttu-id="07715-136">執行的最小開始時間。</span><span class="sxs-lookup"><span data-stu-id="07715-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07715-137">-狀態</span><span class="sxs-lookup"><span data-stu-id="07715-137">-Status</span></span>
<span data-ttu-id="07715-138">執行狀態。</span><span class="sxs-lookup"><span data-stu-id="07715-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07715-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07715-139">CommonParameters</span></span>
<span data-ttu-id="07715-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07715-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07715-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="07715-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07715-142">輸入</span><span class="sxs-lookup"><span data-stu-id="07715-142">INPUTS</span></span>

### <span data-ttu-id="07715-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="07715-143">System.Guid</span></span>

### <span data-ttu-id="07715-144">System.String</span><span class="sxs-lookup"><span data-stu-id="07715-144">System.String</span></span>

### <span data-ttu-id="07715-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="07715-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="07715-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType， Microsoft.Azure.PowerShell.Cmdlets.Automation， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="07715-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="07715-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus， Microsoft.Azure.PowerShell.Cmdlets.Automation， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="07715-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="07715-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="07715-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="07715-149">輸出</span><span class="sxs-lookup"><span data-stu-id="07715-149">OUTPUTS</span></span>

### <span data-ttu-id="07715-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="07715-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="07715-151">筆記</span><span class="sxs-lookup"><span data-stu-id="07715-151">NOTES</span></span>

## <span data-ttu-id="07715-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="07715-152">RELATED LINKS</span></span>
