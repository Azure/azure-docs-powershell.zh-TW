---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 3bb0f095550394991bb74065e8d1c34c346b0c4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902646"
---
# <span data-ttu-id="a4ba2-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a4ba2-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="a4ba2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a4ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ba2-103">在自動化中獲得 DSC 節點組配置部署工作排程。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="a4ba2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a4ba2-104">SYNTAX</span></span>

### <span data-ttu-id="a4ba2-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a4ba2-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ba2-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="a4ba2-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4ba2-107">描述</span><span class="sxs-lookup"><span data-stu-id="a4ba2-107">DESCRIPTION</span></span>
<span data-ttu-id="a4ba2-108">**Get-AzAutomationDscNodeConfigurationDeployment** Cmdlet 在 Azure Automation 中部署 APS 想要的狀態組態 (DSC) 節點組態。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="a4ba2-109">例子</span><span class="sxs-lookup"><span data-stu-id="a4ba2-109">EXAMPLES</span></span>

### <span data-ttu-id="a4ba2-110">範例 1：取得所有部署排程</span><span class="sxs-lookup"><span data-stu-id="a4ba2-110">Example 1: Get all the deployment schedules</span></span>
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

### <span data-ttu-id="a4ba2-111">範例 2：取得部署排程</span><span class="sxs-lookup"><span data-stu-id="a4ba2-111">Example 2: Get a deployment schedule</span></span>
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

<span data-ttu-id="a4ba2-112">上述命令將名為「Config01.Node1」的 DSC 節點組式部署至指定的二維節點名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="a4ba2-113">部署會以階段的方式執行。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="a4ba2-114">參數</span><span class="sxs-lookup"><span data-stu-id="a4ba2-114">PARAMETERS</span></span>

### <span data-ttu-id="a4ba2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4ba2-115">-AutomationAccountName</span></span>
<span data-ttu-id="a4ba2-116">指定包含此 Cmdlet 編譯之 DSC 配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="a4ba2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ba2-117">-DefaultProfile</span></span>
<span data-ttu-id="a4ba2-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a4ba2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4ba2-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="a4ba2-119">-JobScheduleId</span></span>
<span data-ttu-id="a4ba2-120">指定現有已排程部署工作的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="a4ba2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ba2-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4ba2-122">指定此 Cmdlet 編譯群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="a4ba2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ba2-123">CommonParameters</span></span>
<span data-ttu-id="a4ba2-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ba2-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a4ba2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ba2-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a4ba2-126">INPUTS</span></span>

### <span data-ttu-id="a4ba2-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a4ba2-127">System.Guid</span></span>

### <span data-ttu-id="a4ba2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a4ba2-128">System.String</span></span>

## <span data-ttu-id="a4ba2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a4ba2-129">OUTPUTS</span></span>

### <span data-ttu-id="a4ba2-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a4ba2-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="a4ba2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a4ba2-131">NOTES</span></span>

## <span data-ttu-id="a4ba2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4ba2-132">RELATED LINKS</span></span>

[<span data-ttu-id="a4ba2-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a4ba2-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="a4ba2-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4ba2-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a4ba2-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a4ba2-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a4ba2-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a4ba2-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a4ba2-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a4ba2-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
