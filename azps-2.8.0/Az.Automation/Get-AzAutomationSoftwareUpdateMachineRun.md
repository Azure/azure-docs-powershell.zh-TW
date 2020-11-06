---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 80bba3309c0c23862fdb5efbbe6f373b8d1a964a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613769"
---
# <span data-ttu-id="0a295-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="0a295-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="0a295-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a295-102">SYNOPSIS</span></span>
<span data-ttu-id="0a295-103">取得 azure 自動化軟體更新配置電腦的清單。</span><span class="sxs-lookup"><span data-stu-id="0a295-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="0a295-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a295-104">SYNTAX</span></span>

### <span data-ttu-id="0a295-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="0a295-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a295-106">ById</span><span class="sxs-lookup"><span data-stu-id="0a295-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a295-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="0a295-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a295-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="0a295-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a295-109">說明</span><span class="sxs-lookup"><span data-stu-id="0a295-109">DESCRIPTION</span></span>
<span data-ttu-id="0a295-110">這個 Cmdlet 會傳回電腦執行的清單。</span><span class="sxs-lookup"><span data-stu-id="0a295-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="0a295-111">每個軟體更新執行都會觸發針對每個軟體更新設定目的電腦執行的電腦。</span><span class="sxs-lookup"><span data-stu-id="0a295-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="0a295-112">若要執行特定電腦，請傳送 Id 參數。</span><span class="sxs-lookup"><span data-stu-id="0a295-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="0a295-113">您可以列出所有電腦執行、特定電腦的所有執行，並傳遞對應的參數，以特定狀態執行所有工作。</span><span class="sxs-lookup"><span data-stu-id="0a295-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="0a295-114">示例</span><span class="sxs-lookup"><span data-stu-id="0a295-114">EXAMPLES</span></span>

### <span data-ttu-id="0a295-115">範例1</span><span class="sxs-lookup"><span data-stu-id="0a295-115">Example 1</span></span>
<span data-ttu-id="0a295-116">這個範例會為指定的 azure 虛擬機器傳回所有失敗的電腦執行。</span><span class="sxs-lookup"><span data-stu-id="0a295-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


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

## <span data-ttu-id="0a295-117">參數</span><span class="sxs-lookup"><span data-stu-id="0a295-117">PARAMETERS</span></span>

### <span data-ttu-id="0a295-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a295-118">-AutomationAccountName</span></span>
<span data-ttu-id="0a295-119">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0a295-119">The automation account name.</span></span>

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

### <span data-ttu-id="0a295-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a295-120">-DefaultProfile</span></span>
<span data-ttu-id="0a295-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a295-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a295-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0a295-122">-Id</span></span>
<span data-ttu-id="0a295-123">軟體更新電腦執行的 Id。</span><span class="sxs-lookup"><span data-stu-id="0a295-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="0a295-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a295-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a295-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a295-125">The resource group name.</span></span>

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

### <span data-ttu-id="0a295-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="0a295-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="0a295-127">軟體更新執行。</span><span class="sxs-lookup"><span data-stu-id="0a295-127">The software update run.</span></span>

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

### <span data-ttu-id="0a295-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="0a295-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="0a295-129">軟體更新執行的 Id。</span><span class="sxs-lookup"><span data-stu-id="0a295-129">Id of the software update run.</span></span>

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

### <span data-ttu-id="0a295-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="0a295-130">-Status</span></span>
<span data-ttu-id="0a295-131">電腦執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a295-131">Status of the machine run.</span></span>

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

### <span data-ttu-id="0a295-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="0a295-132">-TargetComputer</span></span>
<span data-ttu-id="0a295-133">電腦的目的電腦執行。</span><span class="sxs-lookup"><span data-stu-id="0a295-133">target computer for the machine run.</span></span>
<span data-ttu-id="0a295-134">可以是一個非 az 的電腦名稱稱或 azure VM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="0a295-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

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

### <span data-ttu-id="0a295-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a295-135">CommonParameters</span></span>
<span data-ttu-id="0a295-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a295-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a295-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a295-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a295-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0a295-138">INPUTS</span></span>

### <span data-ttu-id="0a295-139">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="0a295-139">System.Guid</span></span>

### <span data-ttu-id="0a295-140">UpdateManagement SoftwareUpdateRun 中的 []</span><span class="sxs-lookup"><span data-stu-id="0a295-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="0a295-141">"UpdateManagement" 1 [[SoftwareUpdateMachineRunStatus]、[]、[system.object]、[Version = 1.0.0.0]、[Culture = 中立]、[PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0a295-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0a295-142">System.object</span><span class="sxs-lookup"><span data-stu-id="0a295-142">System.String</span></span>

## <span data-ttu-id="0a295-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0a295-143">OUTPUTS</span></span>

### <span data-ttu-id="0a295-144">UpdateManagement SoftwareUpdateMachineRun 中的 []</span><span class="sxs-lookup"><span data-stu-id="0a295-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="0a295-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0a295-145">NOTES</span></span>

## <span data-ttu-id="0a295-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a295-146">RELATED LINKS</span></span>