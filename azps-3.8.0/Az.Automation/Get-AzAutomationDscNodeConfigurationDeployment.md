---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958642"
---
# <span data-ttu-id="8c2ff-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="8c2ff-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="8c2ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2ff-103">在自動化中取得 DSC 節點配置部署。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="8c2ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c2ff-104">SYNTAX</span></span>

### <span data-ttu-id="8c2ff-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="8c2ff-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c2ff-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="8c2ff-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c2ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c2ff-107">DESCRIPTION</span></span>
<span data-ttu-id="8c2ff-108">**AzAutomationDscNodeConfigurationDeployment** Cmdlet 會在 Azure 自動化中 (DSC) 節點設定中，部署 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="8c2ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c2ff-109">EXAMPLES</span></span>

### <span data-ttu-id="8c2ff-110">範例1：取得節點配置部署</span><span class="sxs-lookup"><span data-stu-id="8c2ff-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="8c2ff-111">上述命令會將名為 "Config01. 節點" 的 DSC 節點配置部署到指定的節點名稱二維陣列中。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="8c2ff-112">部署會以分段的方式進行。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="8c2ff-113">參數</span><span class="sxs-lookup"><span data-stu-id="8c2ff-113">PARAMETERS</span></span>

### <span data-ttu-id="8c2ff-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8c2ff-114">-AutomationAccountName</span></span>
<span data-ttu-id="8c2ff-115">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="8c2ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2ff-116">-DefaultProfile</span></span>
<span data-ttu-id="8c2ff-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8c2ff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c2ff-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8c2ff-118">-EndTime</span></span>
<span data-ttu-id="8c2ff-119">[結束時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-119">End time filter.</span></span>

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

### <span data-ttu-id="8c2ff-120">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="8c2ff-120">-JobId</span></span>
<span data-ttu-id="8c2ff-121">指定現有部署作業的作業 id。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="8c2ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c2ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c2ff-123">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="8c2ff-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8c2ff-124">-StartTime</span></span>
<span data-ttu-id="8c2ff-125">[開始時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-125">Start time filter.</span></span>

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

### <span data-ttu-id="8c2ff-126">-狀態</span><span class="sxs-lookup"><span data-stu-id="8c2ff-126">-Status</span></span>
<span data-ttu-id="8c2ff-127">作業篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="8c2ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2ff-128">CommonParameters</span></span>
<span data-ttu-id="8c2ff-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2ff-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c2ff-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2ff-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8c2ff-131">INPUTS</span></span>

### <span data-ttu-id="8c2ff-132">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="8c2ff-132">System.Guid</span></span>

### <span data-ttu-id="8c2ff-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8c2ff-133">System.String</span></span>

## <span data-ttu-id="8c2ff-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8c2ff-134">OUTPUTS</span></span>

### <span data-ttu-id="8c2ff-135">NodeConfigurationDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c2ff-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="8c2ff-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8c2ff-136">NOTES</span></span>

## <span data-ttu-id="8c2ff-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c2ff-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c2ff-138">開始-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="8c2ff-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="8c2ff-139">匯入-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c2ff-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="8c2ff-140">開始-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="8c2ff-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="8c2ff-141">停止 AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="8c2ff-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="8c2ff-142">AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="8c2ff-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
