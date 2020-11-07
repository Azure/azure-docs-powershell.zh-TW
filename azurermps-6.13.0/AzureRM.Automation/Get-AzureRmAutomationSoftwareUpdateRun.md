---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d49d99f8edd3ffe0c25886447eac0bbd15837fc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624933"
---
# <span data-ttu-id="ca69b-101">Get-AzureRmAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ca69b-101">Get-AzureRmAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="ca69b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca69b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca69b-103">取得 azure 自動化軟體更新執行的清單。</span><span class="sxs-lookup"><span data-stu-id="ca69b-103">Gets a list of azure automation software update runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca69b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca69b-104">SYNTAX</span></span>

### <span data-ttu-id="ca69b-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="ca69b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>]
 [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca69b-106">ById</span><span class="sxs-lookup"><span data-stu-id="ca69b-106">ById</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca69b-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="ca69b-107">BySucName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca69b-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="ca69b-108">BySuc</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca69b-109">說明</span><span class="sxs-lookup"><span data-stu-id="ca69b-109">DESCRIPTION</span></span>
<span data-ttu-id="ca69b-110">Get-AzureRmAutomationSoftwareUpdateRun Cmdlet 會傳回軟體更新執行的清單。</span><span class="sxs-lookup"><span data-stu-id="ca69b-110">The Get-AzureRmAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="ca69b-111">因為軟體更新設定有關聯的排程，所以可以多次觸發。</span><span class="sxs-lookup"><span data-stu-id="ca69b-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="ca69b-112">每次觸發排程時，都會產生已建立的更新執行。</span><span class="sxs-lookup"><span data-stu-id="ca69b-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="ca69b-113">[更新執行] 是所有電腦執行結果的匯總。</span><span class="sxs-lookup"><span data-stu-id="ca69b-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="ca69b-114">您可以傳送 SoftwareUpdateConfigurationName 參數，以取得特定軟體更新設定的執行。</span><span class="sxs-lookup"><span data-stu-id="ca69b-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="ca69b-115">若要取得特定的執行，您必須傳遞 name 參數。</span><span class="sxs-lookup"><span data-stu-id="ca69b-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="ca69b-116">您也可以使用特定狀態列出執行，並以特定的 operatins 系統為目標，或傳遞適當的參數，在特定時間之後執行。</span><span class="sxs-lookup"><span data-stu-id="ca69b-116">You can also list runs with specific status, runs targeting specific operatins system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="ca69b-117">示例</span><span class="sxs-lookup"><span data-stu-id="ca69b-117">EXAMPLES</span></span>

### <span data-ttu-id="ca69b-118">範例1</span><span class="sxs-lookup"><span data-stu-id="ca69b-118">Example 1</span></span>
<span data-ttu-id="ca69b-119">這個範例會列出由特定軟體更新設定所觸發的所有更新執行。</span><span class="sxs-lookup"><span data-stu-id="ca69b-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
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

## <span data-ttu-id="ca69b-120">參數</span><span class="sxs-lookup"><span data-stu-id="ca69b-120">PARAMETERS</span></span>

### <span data-ttu-id="ca69b-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca69b-121">-AutomationAccountName</span></span>
<span data-ttu-id="ca69b-122">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ca69b-122">The automation account name.</span></span>

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

### <span data-ttu-id="ca69b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca69b-123">-DefaultProfile</span></span>
<span data-ttu-id="ca69b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca69b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca69b-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ca69b-125">-Id</span></span>
<span data-ttu-id="ca69b-126">執行軟體更新設定的 Id。</span><span class="sxs-lookup"><span data-stu-id="ca69b-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="ca69b-127">-作業系統</span><span class="sxs-lookup"><span data-stu-id="ca69b-127">-OperatingSystem</span></span>
<span data-ttu-id="ca69b-128">執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ca69b-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="ca69b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca69b-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca69b-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca69b-130">The resource group name.</span></span>

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

### <span data-ttu-id="ca69b-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca69b-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="ca69b-132">軟體更新設定觸發了執行。</span><span class="sxs-lookup"><span data-stu-id="ca69b-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="ca69b-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ca69b-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="ca69b-134">已觸發 run 的軟體更新配置名稱。</span><span class="sxs-lookup"><span data-stu-id="ca69b-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="ca69b-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ca69b-135">-StartTime</span></span>
<span data-ttu-id="ca69b-136">執行的最小開始時間。</span><span class="sxs-lookup"><span data-stu-id="ca69b-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="ca69b-137">-狀態</span><span class="sxs-lookup"><span data-stu-id="ca69b-137">-Status</span></span>
<span data-ttu-id="ca69b-138">執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="ca69b-138">Status of the run.</span></span>

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

### <span data-ttu-id="ca69b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca69b-139">CommonParameters</span></span>
<span data-ttu-id="ca69b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca69b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca69b-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca69b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca69b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ca69b-142">INPUTS</span></span>

### <span data-ttu-id="ca69b-143">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="ca69b-143">System.Guid</span></span>

### <span data-ttu-id="ca69b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="ca69b-144">System.String</span></span>

### <span data-ttu-id="ca69b-145">UpdateManagement SoftwareUpdateConfiguration 中的 []</span><span class="sxs-lookup"><span data-stu-id="ca69b-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="ca69b-146">"UpdateManagement" 1 [[5.1.1.0，OperatingSystemType，，"Version =，Culture = 中性，PublicKeyToken = null"]]））。）</span><span class="sxs-lookup"><span data-stu-id="ca69b-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ca69b-147">"UpdateManagement" 1 [[5.1.1.0，SoftwareUpdateRunStatus，，"Version =，Culture = 中性，PublicKeyToken = null"]]））。）</span><span class="sxs-lookup"><span data-stu-id="ca69b-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ca69b-148">System.object</span><span class="sxs-lookup"><span data-stu-id="ca69b-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="ca69b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ca69b-149">OUTPUTS</span></span>

### <span data-ttu-id="ca69b-150">UpdateManagement SoftwareUpdateRun 中的 []</span><span class="sxs-lookup"><span data-stu-id="ca69b-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="ca69b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ca69b-151">NOTES</span></span>

## <span data-ttu-id="ca69b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca69b-152">RELATED LINKS</span></span>
