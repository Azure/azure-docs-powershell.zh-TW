---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 0c918328eb0b578eae31994c949210d62eba337b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448484"
---
# <span data-ttu-id="b12aa-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b12aa-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="b12aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b12aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b12aa-103">在自動化中取得 DSC 節點配置部署。</span><span class="sxs-lookup"><span data-stu-id="b12aa-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b12aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="b12aa-104">SYNTAX</span></span>

### <span data-ttu-id="b12aa-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="b12aa-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b12aa-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b12aa-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b12aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="b12aa-107">DESCRIPTION</span></span>
<span data-ttu-id="b12aa-108">**AzureRmAutomationDscNodeConfigurationDeployment** Cmdlet 會 Deployes Azure 自動化中 (DSC) 節點設定中的 Ap 所需狀態設定。</span><span class="sxs-lookup"><span data-stu-id="b12aa-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="b12aa-109">示例</span><span class="sxs-lookup"><span data-stu-id="b12aa-109">EXAMPLES</span></span>

### <span data-ttu-id="b12aa-110">範例1：取得節點配置部署</span><span class="sxs-lookup"><span data-stu-id="b12aa-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="b12aa-111">上述命令會將名為 "Config01. 節點" 的 DSC 節點配置部署到指定的節點名稱二維陣列中。</span><span class="sxs-lookup"><span data-stu-id="b12aa-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="b12aa-112">部署會以分段的方式進行。</span><span class="sxs-lookup"><span data-stu-id="b12aa-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="b12aa-113">參數</span><span class="sxs-lookup"><span data-stu-id="b12aa-113">PARAMETERS</span></span>

### <span data-ttu-id="b12aa-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b12aa-114">-AutomationAccountName</span></span>
<span data-ttu-id="b12aa-115">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b12aa-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="b12aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12aa-116">-DefaultProfile</span></span>
<span data-ttu-id="b12aa-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b12aa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b12aa-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b12aa-118">-EndTime</span></span>
<span data-ttu-id="b12aa-119">[結束時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="b12aa-119">End time filter.</span></span>

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

### <span data-ttu-id="b12aa-120">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="b12aa-120">-JobId</span></span>
<span data-ttu-id="b12aa-121">指定現有部署作業的作業 id。</span><span class="sxs-lookup"><span data-stu-id="b12aa-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="b12aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b12aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="b12aa-123">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b12aa-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="b12aa-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b12aa-124">-StartTime</span></span>
<span data-ttu-id="b12aa-125">[開始時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="b12aa-125">Start time filter.</span></span>

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

### <span data-ttu-id="b12aa-126">-狀態</span><span class="sxs-lookup"><span data-stu-id="b12aa-126">-Status</span></span>
<span data-ttu-id="b12aa-127">作業篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="b12aa-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="b12aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12aa-128">CommonParameters</span></span>
<span data-ttu-id="b12aa-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b12aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12aa-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b12aa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12aa-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b12aa-131">INPUTS</span></span>

### <span data-ttu-id="b12aa-132">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="b12aa-132">System.Guid</span></span>

### <span data-ttu-id="b12aa-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b12aa-133">System.String</span></span>

## <span data-ttu-id="b12aa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b12aa-134">OUTPUTS</span></span>

### <span data-ttu-id="b12aa-135">NodeConfigurationDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b12aa-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="b12aa-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b12aa-136">NOTES</span></span>

## <span data-ttu-id="b12aa-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b12aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="b12aa-138">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b12aa-138">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="b12aa-139">匯入-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b12aa-139">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="b12aa-140">開始-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b12aa-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b12aa-141">停止 AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b12aa-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b12aa-142">AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="b12aa-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
