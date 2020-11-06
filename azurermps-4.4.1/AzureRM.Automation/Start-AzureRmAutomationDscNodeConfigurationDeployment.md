---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f822f6060827718945f12f998662caeee3b349eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452603"
---
# <span data-ttu-id="aa045-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aa045-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="aa045-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa045-102">SYNOPSIS</span></span>
<span data-ttu-id="aa045-103">在自動化中部署 DSC 節點配置。</span><span class="sxs-lookup"><span data-stu-id="aa045-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa045-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa045-104">SYNTAX</span></span>

### <span data-ttu-id="aa045-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="aa045-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa045-106">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa045-106">ByByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa045-107">說明</span><span class="sxs-lookup"><span data-stu-id="aa045-107">DESCRIPTION</span></span>
<span data-ttu-id="aa045-108">**AzureRmAutomationDscNodeConfigurationDeployment** Cmdlet 會 Deployes Azure 自動化中 (DSC) 節點設定所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="aa045-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="aa045-109">示例</span><span class="sxs-lookup"><span data-stu-id="aa045-109">EXAMPLES</span></span>

### <span data-ttu-id="aa045-110">範例1：在自動化中部署 Azure DSC 節點配置</span><span class="sxs-lookup"><span data-stu-id="aa045-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="aa045-111">上述命令會將名為 "Config01. 節點" 的 DSC 節點配置部署到指定的節點名稱二維陣列中。</span><span class="sxs-lookup"><span data-stu-id="aa045-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="aa045-112">部署會以分段的方式進行。</span><span class="sxs-lookup"><span data-stu-id="aa045-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="aa045-113">範例2：在自動化中排程 Azure DSC 節點配置部署</span><span class="sxs-lookup"><span data-stu-id="aa045-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="aa045-114">上述命令會將名為「Config01. 節點」的 DSC 節點配置的部署，排程至節點名稱的指定二維陣列。</span><span class="sxs-lookup"><span data-stu-id="aa045-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="aa045-115">部署會以分段的方式進行，並根據排程來執行。</span><span class="sxs-lookup"><span data-stu-id="aa045-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="aa045-116">參數</span><span class="sxs-lookup"><span data-stu-id="aa045-116">PARAMETERS</span></span>

### <span data-ttu-id="aa045-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa045-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa045-118">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa045-118">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="aa045-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa045-119">-AutomationAccountName</span></span>
<span data-ttu-id="aa045-120">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="aa045-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="aa045-121">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="aa045-121">-NodeConfigurationName</span></span>
<span data-ttu-id="aa045-122">指定此 Cmdlet 部署之 DSC 節點設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa045-122">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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
Parameter Sets: ByByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa045-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="aa045-123">-NodeName</span></span>
<span data-ttu-id="aa045-124">指定要將節點配置部署到哪個節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa045-124">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="aa045-125">-排程</span><span class="sxs-lookup"><span data-stu-id="aa045-125">-Schedule</span></span>
<span data-ttu-id="aa045-126">[自動化排程] 物件來排程部署作業。</span><span class="sxs-lookup"><span data-stu-id="aa045-126">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="aa045-127">-Force</span><span class="sxs-lookup"><span data-stu-id="aa045-127">-Force</span></span>
<span data-ttu-id="aa045-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="aa045-128">ps_force</span></span>

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

### <span data-ttu-id="aa045-129">-確認</span><span class="sxs-lookup"><span data-stu-id="aa045-129">-Confirm</span></span>
<span data-ttu-id="aa045-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa045-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa045-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa045-131">-WhatIf</span></span>
<span data-ttu-id="aa045-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa045-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa045-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa045-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa045-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa045-134">-DefaultProfile</span></span>
<span data-ttu-id="aa045-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa045-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa045-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa045-136">-InputObject</span></span>
<span data-ttu-id="aa045-137">[管道] 的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="aa045-137">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa045-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa045-138">CommonParameters</span></span>
<span data-ttu-id="aa045-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa045-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa045-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa045-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa045-141">輸入</span><span class="sxs-lookup"><span data-stu-id="aa045-141">INPUTS</span></span>

## <span data-ttu-id="aa045-142">輸出</span><span class="sxs-lookup"><span data-stu-id="aa045-142">OUTPUTS</span></span>

### <span data-ttu-id="aa045-143">NodeConfigurationDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aa045-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="aa045-144">筆記</span><span class="sxs-lookup"><span data-stu-id="aa045-144">NOTES</span></span>

## <span data-ttu-id="aa045-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa045-145">RELATED LINKS</span></span>

[<span data-ttu-id="aa045-146">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="aa045-146">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="aa045-147">匯入-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa045-147">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="aa045-148">停止 AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aa045-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="aa045-149">AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aa045-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="aa045-150">AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="aa045-150">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="aa045-151">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aa045-151">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
