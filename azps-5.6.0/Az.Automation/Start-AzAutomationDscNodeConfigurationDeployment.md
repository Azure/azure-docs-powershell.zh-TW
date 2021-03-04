---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 477b8f5853d9a5dbe3dd030e7419316825088807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903350"
---
# <span data-ttu-id="a07e6-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a07e6-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="a07e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a07e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a07e6-103">在自動化中部署 DSC 節點組。</span><span class="sxs-lookup"><span data-stu-id="a07e6-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="a07e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="a07e6-104">SYNTAX</span></span>

### <span data-ttu-id="a07e6-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a07e6-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a07e6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a07e6-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a07e6-107">描述</span><span class="sxs-lookup"><span data-stu-id="a07e6-107">DESCRIPTION</span></span>
<span data-ttu-id="a07e6-108">**Start-AzAutomationDscNodeConfigurationDeployment** Cmdlet 在 Azure Automation 中部署想要的狀態組態 (DSC) 節點組態。</span><span class="sxs-lookup"><span data-stu-id="a07e6-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="a07e6-109">例子</span><span class="sxs-lookup"><span data-stu-id="a07e6-109">EXAMPLES</span></span>

### <span data-ttu-id="a07e6-110">範例 1：在自動化中部署 Azure DSC 節點組</span><span class="sxs-lookup"><span data-stu-id="a07e6-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a07e6-111">上述命令將名為「Config01.Node1」的 DSC 節點組式部署至指定的二維節點名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="a07e6-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="a07e6-112">部署會以階段的方式執行。</span><span class="sxs-lookup"><span data-stu-id="a07e6-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="a07e6-113">範例 2：在自動化中排程 Azure DSC 節點組組部署</span><span class="sxs-lookup"><span data-stu-id="a07e6-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="a07e6-114">上述命令會排程將名為 "Config01.Node1" 的 DSC 節點組式部署排程至指定的二維節點名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="a07e6-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="a07e6-115">部署會以階段的方式執行，並且會根據排程執行。</span><span class="sxs-lookup"><span data-stu-id="a07e6-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="a07e6-116">參數</span><span class="sxs-lookup"><span data-stu-id="a07e6-116">PARAMETERS</span></span>

### <span data-ttu-id="a07e6-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a07e6-117">-AutomationAccountName</span></span>
<span data-ttu-id="a07e6-118">指定包含此 Cmdlet 編譯之 DSC 配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a07e6-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="a07e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07e6-119">-DefaultProfile</span></span>
<span data-ttu-id="a07e6-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a07e6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a07e6-121">-強制</span><span class="sxs-lookup"><span data-stu-id="a07e6-121">-Force</span></span>
<span data-ttu-id="a07e6-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="a07e6-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a07e6-123">-InputObject</span></span>
<span data-ttu-id="a07e6-124">用於管線的輸入物件</span><span class="sxs-lookup"><span data-stu-id="a07e6-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a07e6-125">-NodeConfigurationName</span></span>
<span data-ttu-id="a07e6-126">指定此 Cmdlet 部署之 DSC 節點組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a07e6-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a07e6-127">-NodeName</span></span>
<span data-ttu-id="a07e6-128">指定節點組調要部署至的節點名稱。</span><span class="sxs-lookup"><span data-stu-id="a07e6-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07e6-129">-ResourceGroupName</span></span>
<span data-ttu-id="a07e6-130">指定此 Cmdlet 編譯群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a07e6-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="a07e6-131">-排程</span><span class="sxs-lookup"><span data-stu-id="a07e6-131">-Schedule</span></span>
<span data-ttu-id="a07e6-132">自動化排程物件以排程部署工作。</span><span class="sxs-lookup"><span data-stu-id="a07e6-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a07e6-133">-Confirm</span></span>
<span data-ttu-id="a07e6-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a07e6-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07e6-135">-WhatIf</span></span>
<span data-ttu-id="a07e6-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a07e6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07e6-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a07e6-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07e6-138">CommonParameters</span></span>
<span data-ttu-id="a07e6-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a07e6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07e6-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a07e6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07e6-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a07e6-141">INPUTS</span></span>

### <span data-ttu-id="a07e6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a07e6-142">System.String</span></span>

### <span data-ttu-id="a07e6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a07e6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="a07e6-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a07e6-144">OUTPUTS</span></span>

### <span data-ttu-id="a07e6-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a07e6-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="a07e6-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a07e6-146">NOTES</span></span>

## <span data-ttu-id="a07e6-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a07e6-147">RELATED LINKS</span></span>

[<span data-ttu-id="a07e6-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a07e6-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="a07e6-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a07e6-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a07e6-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a07e6-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a07e6-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a07e6-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a07e6-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a07e6-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="a07e6-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a07e6-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
