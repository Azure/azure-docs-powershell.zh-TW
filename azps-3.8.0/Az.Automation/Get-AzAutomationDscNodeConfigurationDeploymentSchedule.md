---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: bc98d8ed8773e49eab594a4d715bef3f93862e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958644"
---
# <span data-ttu-id="3fb08-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="3fb08-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="3fb08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fb08-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb08-103">在自動化中取得 DSC 節點配置部署作業排程。</span><span class="sxs-lookup"><span data-stu-id="3fb08-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="3fb08-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fb08-104">SYNTAX</span></span>

### <span data-ttu-id="3fb08-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="3fb08-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fb08-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="3fb08-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fb08-107">說明</span><span class="sxs-lookup"><span data-stu-id="3fb08-107">DESCRIPTION</span></span>
<span data-ttu-id="3fb08-108">**AzAutomationDscNodeConfigurationDeployment** Cmdlet 會在 Azure 自動化中 (DSC) 節點設定中，部署 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="3fb08-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="3fb08-109">示例</span><span class="sxs-lookup"><span data-stu-id="3fb08-109">EXAMPLES</span></span>

### <span data-ttu-id="3fb08-110">範例1：取得所有部署排程</span><span class="sxs-lookup"><span data-stu-id="3fb08-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="3fb08-111">範例2：取得部署排程</span><span class="sxs-lookup"><span data-stu-id="3fb08-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="3fb08-112">上述命令會將名為 "Config01. 節點" 的 DSC 節點配置部署到指定的節點名稱二維陣列中。</span><span class="sxs-lookup"><span data-stu-id="3fb08-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="3fb08-113">部署會以分段的方式進行。</span><span class="sxs-lookup"><span data-stu-id="3fb08-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="3fb08-114">參數</span><span class="sxs-lookup"><span data-stu-id="3fb08-114">PARAMETERS</span></span>

### <span data-ttu-id="3fb08-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3fb08-115">-AutomationAccountName</span></span>
<span data-ttu-id="3fb08-116">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3fb08-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="3fb08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb08-117">-DefaultProfile</span></span>
<span data-ttu-id="3fb08-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3fb08-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fb08-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="3fb08-119">-JobScheduleId</span></span>
<span data-ttu-id="3fb08-120">指定現有排程部署作業的作業排程 id。</span><span class="sxs-lookup"><span data-stu-id="3fb08-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb08-121">-ResourceGroupName</span></span>
<span data-ttu-id="3fb08-122">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fb08-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="3fb08-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb08-123">CommonParameters</span></span>
<span data-ttu-id="3fb08-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fb08-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb08-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fb08-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb08-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3fb08-126">INPUTS</span></span>

### <span data-ttu-id="3fb08-127">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="3fb08-127">System.Guid</span></span>

### <span data-ttu-id="3fb08-128">System.object</span><span class="sxs-lookup"><span data-stu-id="3fb08-128">System.String</span></span>

## <span data-ttu-id="3fb08-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3fb08-129">OUTPUTS</span></span>

### <span data-ttu-id="3fb08-130">NodeConfigurationDeploymentSchedule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3fb08-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="3fb08-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3fb08-131">NOTES</span></span>

## <span data-ttu-id="3fb08-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fb08-132">RELATED LINKS</span></span>

[<span data-ttu-id="3fb08-133">開始-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="3fb08-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="3fb08-134">匯入-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fb08-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="3fb08-135">開始-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3fb08-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="3fb08-136">停止 AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3fb08-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="3fb08-137">AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3fb08-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
