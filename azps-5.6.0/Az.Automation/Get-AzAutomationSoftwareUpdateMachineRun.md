---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 9a9a79dbd09c91a77af8982ea367498061b2ee1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917469"
---
# <span data-ttu-id="45095-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="45095-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="45095-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45095-102">SYNOPSIS</span></span>
<span data-ttu-id="45095-103">獲得 Azure 自動化軟體更新組組機器執行的清單。</span><span class="sxs-lookup"><span data-stu-id="45095-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="45095-104">語法</span><span class="sxs-lookup"><span data-stu-id="45095-104">SYNTAX</span></span>

### <span data-ttu-id="45095-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="45095-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45095-106">ById</span><span class="sxs-lookup"><span data-stu-id="45095-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45095-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="45095-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45095-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="45095-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45095-109">描述</span><span class="sxs-lookup"><span data-stu-id="45095-109">DESCRIPTION</span></span>
<span data-ttu-id="45095-110">此 Cmdlet 會返回電腦執行的清單。</span><span class="sxs-lookup"><span data-stu-id="45095-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="45095-111">每次軟體更新執行都會觸發每個軟體更新組配置目的電腦的機器執行。</span><span class="sxs-lookup"><span data-stu-id="45095-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="45095-112">若要執行特定電腦，請傳遞 Id 參數。</span><span class="sxs-lookup"><span data-stu-id="45095-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="45095-113">您可以列出所有電腦執行，所有執行都適用于特定電腦，所有執行狀態都傳遞對應的參數。</span><span class="sxs-lookup"><span data-stu-id="45095-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="45095-114">例子</span><span class="sxs-lookup"><span data-stu-id="45095-114">EXAMPLES</span></span>

### <span data-ttu-id="45095-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="45095-115">Example 1</span></span>
<span data-ttu-id="45095-116">此範例會針對指定的 Azure 虛擬機器，會執行所有失敗的機器。</span><span class="sxs-lookup"><span data-stu-id="45095-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="45095-117">參數</span><span class="sxs-lookup"><span data-stu-id="45095-117">PARAMETERS</span></span>

### <span data-ttu-id="45095-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="45095-118">-AutomationAccountName</span></span>
<span data-ttu-id="45095-119">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="45095-119">The automation account name.</span></span>

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

### <span data-ttu-id="45095-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45095-120">-DefaultProfile</span></span>
<span data-ttu-id="45095-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45095-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45095-122">-Id</span><span class="sxs-lookup"><span data-stu-id="45095-122">-Id</span></span>
<span data-ttu-id="45095-123">執行軟體更新機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45095-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="45095-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45095-124">-ResourceGroupName</span></span>
<span data-ttu-id="45095-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="45095-125">The resource group name.</span></span>

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

### <span data-ttu-id="45095-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="45095-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="45095-127">軟體更新會執行。</span><span class="sxs-lookup"><span data-stu-id="45095-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45095-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="45095-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="45095-129">執行軟體更新的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45095-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45095-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="45095-130">-Status</span></span>
<span data-ttu-id="45095-131">電腦執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="45095-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45095-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="45095-132">-TargetComputer</span></span>
<span data-ttu-id="45095-133">電腦執行的目的電腦。</span><span class="sxs-lookup"><span data-stu-id="45095-133">target computer for the machine run.</span></span>
<span data-ttu-id="45095-134">可以是非 az 電腦名稱稱或 Azure VM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="45095-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45095-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45095-135">CommonParameters</span></span>
<span data-ttu-id="45095-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45095-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45095-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="45095-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45095-138">輸入</span><span class="sxs-lookup"><span data-stu-id="45095-138">INPUTS</span></span>

### <span data-ttu-id="45095-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="45095-139">System.Guid</span></span>

### <span data-ttu-id="45095-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="45095-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="45095-141">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus， Microsoft.Azure.PowerShell.Cmdlets.Automation， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="45095-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="45095-142">System.String</span><span class="sxs-lookup"><span data-stu-id="45095-142">System.String</span></span>

## <span data-ttu-id="45095-143">輸出</span><span class="sxs-lookup"><span data-stu-id="45095-143">OUTPUTS</span></span>

### <span data-ttu-id="45095-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="45095-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="45095-145">筆記</span><span class="sxs-lookup"><span data-stu-id="45095-145">NOTES</span></span>

## <span data-ttu-id="45095-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="45095-146">RELATED LINKS</span></span>
