---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 726423dfcfef07142002cd40b29b6e4d26f91137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908650"
---
# <span data-ttu-id="ba3ee-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ba3ee-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="ba3ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3ee-103">在自動化中停止 DSC 節點組組部署。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="ba3ee-104">它只會停止目前的部署工作，但是不會取消指派已指派的節點群組原則。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="ba3ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="ba3ee-105">SYNTAX</span></span>

### <span data-ttu-id="ba3ee-106">ByJobId (預設) </span><span class="sxs-lookup"><span data-stu-id="ba3ee-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba3ee-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba3ee-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba3ee-108">描述</span><span class="sxs-lookup"><span data-stu-id="ba3ee-108">DESCRIPTION</span></span>
<span data-ttu-id="ba3ee-109">**Stop-AzAutomationDscNodeConfigurationDeployment** Cmdlet 會停止 Azure Automation 中所需狀態組態 (DSC) 節點組態的部署。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="ba3ee-110">它會停止指派節點組至節點群組的節點組 ，如果有剩餘部分要指派，但是不會取消指派已指派的節點。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="ba3ee-111">若要取消註冊已排程的工作，請使用 [Ungister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) 與 JobScheduleId 來取消分配現有的已排程工作。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="ba3ee-112">例子</span><span class="sxs-lookup"><span data-stu-id="ba3ee-112">EXAMPLES</span></span>

### <span data-ttu-id="ba3ee-113">範例 1：在自動化中部署 Azure DSC 節點組</span><span class="sxs-lookup"><span data-stu-id="ba3ee-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="ba3ee-114">上述命令會停止傳遞 jobId 的 DSC 節點組配置部署工作。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="ba3ee-115">參數</span><span class="sxs-lookup"><span data-stu-id="ba3ee-115">PARAMETERS</span></span>

### <span data-ttu-id="ba3ee-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba3ee-116">-AutomationAccountName</span></span>
<span data-ttu-id="ba3ee-117">指定包含此 Cmdlet 編譯之 DSC 配置的自動化帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ba3ee-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="ba3ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3ee-118">-DefaultProfile</span></span>
<span data-ttu-id="ba3ee-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ba3ee-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba3ee-120">-強制</span><span class="sxs-lookup"><span data-stu-id="ba3ee-120">-Force</span></span>
<span data-ttu-id="ba3ee-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="ba3ee-121">ps_force</span></span>

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

### <span data-ttu-id="ba3ee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba3ee-122">-InputObject</span></span>
<span data-ttu-id="ba3ee-123">用於管線的輸入物件</span><span class="sxs-lookup"><span data-stu-id="ba3ee-123">Input object for Piping</span></span>

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

### <span data-ttu-id="ba3ee-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="ba3ee-124">-JobId</span></span>
<span data-ttu-id="ba3ee-125">指定現有部署工作的 Job ID。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="ba3ee-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba3ee-126">-PassThru</span></span>
<span data-ttu-id="ba3ee-127">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba3ee-128">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba3ee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3ee-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba3ee-130">指定此 Cmdlet 編譯群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="ba3ee-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ba3ee-131">-Confirm</span></span>
<span data-ttu-id="ba3ee-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba3ee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba3ee-133">-WhatIf</span></span>
<span data-ttu-id="ba3ee-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba3ee-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba3ee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3ee-136">CommonParameters</span></span>
<span data-ttu-id="ba3ee-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3ee-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ba3ee-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3ee-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ba3ee-139">INPUTS</span></span>

### <span data-ttu-id="ba3ee-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ba3ee-140">System.Guid</span></span>

### <span data-ttu-id="ba3ee-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ba3ee-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="ba3ee-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ba3ee-142">System.String</span></span>

## <span data-ttu-id="ba3ee-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ba3ee-143">OUTPUTS</span></span>

### <span data-ttu-id="ba3ee-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba3ee-144">System.Boolean</span></span>

## <span data-ttu-id="ba3ee-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ba3ee-145">NOTES</span></span>

## <span data-ttu-id="ba3ee-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba3ee-146">RELATED LINKS</span></span>

[<span data-ttu-id="ba3ee-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ba3ee-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="ba3ee-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba3ee-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ba3ee-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ba3ee-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ba3ee-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ba3ee-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ba3ee-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3ee-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
