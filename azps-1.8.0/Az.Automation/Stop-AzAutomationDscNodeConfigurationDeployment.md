---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 698f0354b9f67896c14b8bb19d3716fa9e9167c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622930"
---
# <span data-ttu-id="fa9be-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="fa9be-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="fa9be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa9be-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9be-103">在自動化中停止 DSC 節點配置部署。</span><span class="sxs-lookup"><span data-stu-id="fa9be-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="fa9be-104">它只會停止目前的部署作業，但不會取消指派已指派的節點配置。</span><span class="sxs-lookup"><span data-stu-id="fa9be-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="fa9be-105">句法</span><span class="sxs-lookup"><span data-stu-id="fa9be-105">SYNTAX</span></span>

### <span data-ttu-id="fa9be-106">ByJobId (預設) </span><span class="sxs-lookup"><span data-stu-id="fa9be-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9be-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa9be-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9be-108">說明</span><span class="sxs-lookup"><span data-stu-id="fa9be-108">DESCRIPTION</span></span>
<span data-ttu-id="fa9be-109">**Stop-AzAutomationDscNodeConfigurationDeployment** Cmdlet 會在 Azure 自動化中停止部署所需的狀態設定 (DSC) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="fa9be-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="fa9be-110">它會停止將節點配置指派給節點群組（如果有剩餘的指派），但不會取消指派已指派的節點。</span><span class="sxs-lookup"><span data-stu-id="fa9be-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="fa9be-111">若要登出排程作業，請在 JobScheduleId 中使用 [ [取消註冊] AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) ，以取消指派現有的排程作業。</span><span class="sxs-lookup"><span data-stu-id="fa9be-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="fa9be-112">示例</span><span class="sxs-lookup"><span data-stu-id="fa9be-112">EXAMPLES</span></span>

### <span data-ttu-id="fa9be-113">範例1：在自動化中部署 Azure DSC 節點配置</span><span class="sxs-lookup"><span data-stu-id="fa9be-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="fa9be-114">上述命令會停止與已傳入作業 Id 的 DSC 節點配置部署作業。</span><span class="sxs-lookup"><span data-stu-id="fa9be-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="fa9be-115">參數</span><span class="sxs-lookup"><span data-stu-id="fa9be-115">PARAMETERS</span></span>

### <span data-ttu-id="fa9be-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fa9be-116">-AutomationAccountName</span></span>
<span data-ttu-id="fa9be-117">指定包含此 Cmdlet 編譯之 DSC 設定的自動化帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="fa9be-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="fa9be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9be-118">-DefaultProfile</span></span>
<span data-ttu-id="fa9be-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa9be-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa9be-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fa9be-120">-Force</span></span>
<span data-ttu-id="fa9be-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="fa9be-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa9be-122">-InputObject</span></span>
<span data-ttu-id="fa9be-123">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="fa9be-123">Input object for Piping</span></span>

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

### <span data-ttu-id="fa9be-124">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="fa9be-124">-JobId</span></span>
<span data-ttu-id="fa9be-125">指定現有部署作業的作業 id。</span><span class="sxs-lookup"><span data-stu-id="fa9be-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="fa9be-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa9be-126">-PassThru</span></span>
<span data-ttu-id="fa9be-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fa9be-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa9be-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fa9be-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa9be-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa9be-130">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa9be-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="fa9be-131">-確認</span><span class="sxs-lookup"><span data-stu-id="fa9be-131">-Confirm</span></span>
<span data-ttu-id="fa9be-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa9be-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9be-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9be-133">-WhatIf</span></span>
<span data-ttu-id="fa9be-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa9be-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9be-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa9be-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9be-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9be-136">CommonParameters</span></span>
<span data-ttu-id="fa9be-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa9be-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9be-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa9be-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9be-139">輸入</span><span class="sxs-lookup"><span data-stu-id="fa9be-139">INPUTS</span></span>

### <span data-ttu-id="fa9be-140">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="fa9be-140">System.Guid</span></span>

### <span data-ttu-id="fa9be-141">NodeConfigurationDeployment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fa9be-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="fa9be-142">System.object</span><span class="sxs-lookup"><span data-stu-id="fa9be-142">System.String</span></span>

## <span data-ttu-id="fa9be-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fa9be-143">OUTPUTS</span></span>

### <span data-ttu-id="fa9be-144">System.object</span><span class="sxs-lookup"><span data-stu-id="fa9be-144">System.Boolean</span></span>

## <span data-ttu-id="fa9be-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fa9be-145">NOTES</span></span>

## <span data-ttu-id="fa9be-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa9be-146">RELATED LINKS</span></span>

[<span data-ttu-id="fa9be-147">開始-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="fa9be-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="fa9be-148">匯入-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa9be-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="fa9be-149">開始-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="fa9be-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="fa9be-150">AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="fa9be-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="fa9be-151">AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="fa9be-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
