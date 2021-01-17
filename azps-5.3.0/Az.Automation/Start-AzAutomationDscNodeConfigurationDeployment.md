---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447095"
---
# <span data-ttu-id="76a57-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="76a57-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="76a57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76a57-102">SYNOPSIS</span></span>
<span data-ttu-id="76a57-103">在自動化中部署 DSC 節點配置。</span><span class="sxs-lookup"><span data-stu-id="76a57-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="76a57-104">句法</span><span class="sxs-lookup"><span data-stu-id="76a57-104">SYNTAX</span></span>

### <span data-ttu-id="76a57-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="76a57-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76a57-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76a57-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a57-107">說明</span><span class="sxs-lookup"><span data-stu-id="76a57-107">DESCRIPTION</span></span>
<span data-ttu-id="76a57-108">**Start-AzAutomationDscNodeConfigurationDeployment** Cmdlet 會在 Azure 自動化中 (DSC) 節點設定中，部署所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="76a57-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="76a57-109">示例</span><span class="sxs-lookup"><span data-stu-id="76a57-109">EXAMPLES</span></span>

### <span data-ttu-id="76a57-110">範例1：在自動化中部署 Azure DSC 節點配置</span><span class="sxs-lookup"><span data-stu-id="76a57-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
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

<span data-ttu-id="76a57-111">上述命令會將名為 "Config01. 節點" 的 DSC 節點配置部署到指定的節點名稱二維陣列中。</span><span class="sxs-lookup"><span data-stu-id="76a57-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="76a57-112">部署會以分段的方式進行。</span><span class="sxs-lookup"><span data-stu-id="76a57-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="76a57-113">範例2：在自動化中排程 Azure DSC 節點配置部署</span><span class="sxs-lookup"><span data-stu-id="76a57-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
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

<span data-ttu-id="76a57-114">上述命令會將名為「Config01. 節點」的 DSC 節點配置的部署，排程至節點名稱的指定二維陣列。</span><span class="sxs-lookup"><span data-stu-id="76a57-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="76a57-115">部署會以分段的方式進行，並根據排程來執行。</span><span class="sxs-lookup"><span data-stu-id="76a57-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="76a57-116">參數</span><span class="sxs-lookup"><span data-stu-id="76a57-116">PARAMETERS</span></span>

### <span data-ttu-id="76a57-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76a57-117">-AutomationAccountName</span></span>
<span data-ttu-id="76a57-118">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="76a57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a57-119">-DefaultProfile</span></span>
<span data-ttu-id="76a57-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="76a57-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76a57-121">-Force</span><span class="sxs-lookup"><span data-stu-id="76a57-121">-Force</span></span>
<span data-ttu-id="76a57-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="76a57-122">ps_force</span></span>

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

### <span data-ttu-id="76a57-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a57-123">-InputObject</span></span>
<span data-ttu-id="76a57-124">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="76a57-124">Input object for Piping</span></span>

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

### <span data-ttu-id="76a57-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="76a57-125">-NodeConfigurationName</span></span>
<span data-ttu-id="76a57-126">指定此 Cmdlet 部署之 DSC 節點設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="76a57-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="76a57-127">-NodeName</span></span>
<span data-ttu-id="76a57-128">指定要將節點配置部署到哪個節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="76a57-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a57-129">-ResourceGroupName</span></span>
<span data-ttu-id="76a57-130">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="76a57-131">-排程</span><span class="sxs-lookup"><span data-stu-id="76a57-131">-Schedule</span></span>
<span data-ttu-id="76a57-132">[自動化排程] 物件來排程部署作業。</span><span class="sxs-lookup"><span data-stu-id="76a57-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="76a57-133">-確認</span><span class="sxs-lookup"><span data-stu-id="76a57-133">-Confirm</span></span>
<span data-ttu-id="76a57-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76a57-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a57-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a57-135">-WhatIf</span></span>
<span data-ttu-id="76a57-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76a57-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a57-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76a57-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a57-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a57-138">CommonParameters</span></span>
<span data-ttu-id="76a57-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76a57-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a57-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76a57-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a57-141">輸入</span><span class="sxs-lookup"><span data-stu-id="76a57-141">INPUTS</span></span>

### <span data-ttu-id="76a57-142">System.object</span><span class="sxs-lookup"><span data-stu-id="76a57-142">System.String</span></span>

### <span data-ttu-id="76a57-143">NodeConfigurationDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76a57-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="76a57-144">輸出</span><span class="sxs-lookup"><span data-stu-id="76a57-144">OUTPUTS</span></span>

### <span data-ttu-id="76a57-145">NodeConfigurationDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76a57-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="76a57-146">筆記</span><span class="sxs-lookup"><span data-stu-id="76a57-146">NOTES</span></span>

## <span data-ttu-id="76a57-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="76a57-147">RELATED LINKS</span></span>

[<span data-ttu-id="76a57-148">開始-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="76a57-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="76a57-149">匯入-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="76a57-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="76a57-150">停止 AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="76a57-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="76a57-151">AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="76a57-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="76a57-152">AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="76a57-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="76a57-153">新-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="76a57-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
