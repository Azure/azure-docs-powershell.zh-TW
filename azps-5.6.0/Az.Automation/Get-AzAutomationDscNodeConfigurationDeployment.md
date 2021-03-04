---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f5cbb59ffbd5b79087e9f338788dde9d1176f4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913261"
---
# <span data-ttu-id="1a026-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1a026-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="1a026-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a026-102">SYNOPSIS</span></span>
<span data-ttu-id="1a026-103">在自動化中進行 DSC 節點組配置部署。</span><span class="sxs-lookup"><span data-stu-id="1a026-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="1a026-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a026-104">SYNTAX</span></span>

### <span data-ttu-id="1a026-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="1a026-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a026-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="1a026-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a026-107">描述</span><span class="sxs-lookup"><span data-stu-id="1a026-107">DESCRIPTION</span></span>
<span data-ttu-id="1a026-108">**Get-AzAutomationDscNodeConfigurationDeployment** Cmdlet 在 Azure Automation 中部署 APS 想要的狀態組態 (DSC) 節點組態。</span><span class="sxs-lookup"><span data-stu-id="1a026-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="1a026-109">例子</span><span class="sxs-lookup"><span data-stu-id="1a026-109">EXAMPLES</span></span>

### <span data-ttu-id="1a026-110">範例 1：取得節點組配置部署</span><span class="sxs-lookup"><span data-stu-id="1a026-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="1a026-111">上述命令將名為「Config01.Node1」的 DSC 節點組式部署至指定的二維節點名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="1a026-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="1a026-112">部署會以階段的方式執行。</span><span class="sxs-lookup"><span data-stu-id="1a026-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="1a026-113">參數</span><span class="sxs-lookup"><span data-stu-id="1a026-113">PARAMETERS</span></span>

### <span data-ttu-id="1a026-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a026-114">-AutomationAccountName</span></span>
<span data-ttu-id="1a026-115">指定包含此 Cmdlet 編譯之 DSC 配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1a026-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="1a026-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a026-116">-DefaultProfile</span></span>
<span data-ttu-id="1a026-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1a026-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a026-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1a026-118">-EndTime</span></span>
<span data-ttu-id="1a026-119">結束時間篩選。</span><span class="sxs-lookup"><span data-stu-id="1a026-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a026-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="1a026-120">-JobId</span></span>
<span data-ttu-id="1a026-121">指定現有部署工作的 Job ID。</span><span class="sxs-lookup"><span data-stu-id="1a026-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a026-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a026-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a026-123">指定此 Cmdlet 編譯群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1a026-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="1a026-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1a026-124">-StartTime</span></span>
<span data-ttu-id="1a026-125">開始時間篩選。</span><span class="sxs-lookup"><span data-stu-id="1a026-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a026-126">-狀態</span><span class="sxs-lookup"><span data-stu-id="1a026-126">-Status</span></span>
<span data-ttu-id="1a026-127">工作篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="1a026-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a026-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a026-128">CommonParameters</span></span>
<span data-ttu-id="1a026-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a026-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a026-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1a026-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a026-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1a026-131">INPUTS</span></span>

### <span data-ttu-id="1a026-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1a026-132">System.Guid</span></span>

### <span data-ttu-id="1a026-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1a026-133">System.String</span></span>

## <span data-ttu-id="1a026-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1a026-134">OUTPUTS</span></span>

### <span data-ttu-id="1a026-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1a026-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="1a026-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1a026-136">NOTES</span></span>

## <span data-ttu-id="1a026-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a026-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a026-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1a026-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="1a026-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a026-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="1a026-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1a026-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="1a026-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1a026-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="1a026-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="1a026-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
