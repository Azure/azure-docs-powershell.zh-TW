---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 17106fed79fdec90bad6615560553dcdb5d46703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625032"
---
# <span data-ttu-id="a11fe-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a11fe-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="a11fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a11fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a11fe-103">在自動化中停止 DSC 節點配置部署。</span><span class="sxs-lookup"><span data-stu-id="a11fe-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="a11fe-104">它只會停止目前的部署作業，但不會取消指派已指派的節點配置。</span><span class="sxs-lookup"><span data-stu-id="a11fe-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a11fe-105">句法</span><span class="sxs-lookup"><span data-stu-id="a11fe-105">SYNTAX</span></span>

### <span data-ttu-id="a11fe-106">ByJobId (預設) </span><span class="sxs-lookup"><span data-stu-id="a11fe-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a11fe-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a11fe-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11fe-108">說明</span><span class="sxs-lookup"><span data-stu-id="a11fe-108">DESCRIPTION</span></span>
<span data-ttu-id="a11fe-109">**Stop-AzureRmAutomationDscNodeConfigurationDeployment** Cmdlet 會在 Azure 自動化中停止部署所需的狀態設定 (DSC) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="a11fe-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="a11fe-110">它會停止將節點配置指派給節點群組（如果有剩餘的指派），但不會取消指派已指派的節點。</span><span class="sxs-lookup"><span data-stu-id="a11fe-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="a11fe-111">若要登出排程作業，請在 JobScheduleId 中使用 [ [取消註冊] AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) ，以取消指派現有的排程作業。</span><span class="sxs-lookup"><span data-stu-id="a11fe-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="a11fe-112">示例</span><span class="sxs-lookup"><span data-stu-id="a11fe-112">EXAMPLES</span></span>

### <span data-ttu-id="a11fe-113">範例1：在自動化中部署 Azure DSC 節點配置</span><span class="sxs-lookup"><span data-stu-id="a11fe-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a11fe-114">上述命令會停止與已傳入作業 Id 的 DSC 節點配置部署作業。</span><span class="sxs-lookup"><span data-stu-id="a11fe-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="a11fe-115">參數</span><span class="sxs-lookup"><span data-stu-id="a11fe-115">PARAMETERS</span></span>

### <span data-ttu-id="a11fe-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a11fe-116">-AutomationAccountName</span></span>
<span data-ttu-id="a11fe-117">指定包含此 Cmdlet 編譯之 DSC 設定的自動化帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="a11fe-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11fe-118">-DefaultProfile</span></span>
<span data-ttu-id="a11fe-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a11fe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a11fe-120">-Force</span></span>
<span data-ttu-id="a11fe-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="a11fe-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a11fe-122">-InputObject</span></span>
<span data-ttu-id="a11fe-123">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="a11fe-123">Input object for Piping</span></span>

```yaml
Type: NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-124">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="a11fe-124">-JobId</span></span>
<span data-ttu-id="a11fe-125">指定現有部署作業的作業 id。</span><span class="sxs-lookup"><span data-stu-id="a11fe-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a11fe-126">-PassThru</span></span>
<span data-ttu-id="a11fe-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a11fe-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a11fe-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a11fe-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="a11fe-130">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a11fe-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a11fe-131">-Confirm</span></span>
<span data-ttu-id="a11fe-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a11fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11fe-133">-WhatIf</span></span>
<span data-ttu-id="a11fe-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a11fe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11fe-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a11fe-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11fe-136">CommonParameters</span></span>
<span data-ttu-id="a11fe-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a11fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11fe-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a11fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11fe-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a11fe-139">INPUTS</span></span>

### <span data-ttu-id="a11fe-140">所有</span><span class="sxs-lookup"><span data-stu-id="a11fe-140">None</span></span>
<span data-ttu-id="a11fe-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a11fe-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a11fe-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a11fe-142">OUTPUTS</span></span>

## <span data-ttu-id="a11fe-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a11fe-143">NOTES</span></span>

## <span data-ttu-id="a11fe-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a11fe-144">RELATED LINKS</span></span>

[<span data-ttu-id="a11fe-145">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a11fe-145">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="a11fe-146">匯入-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a11fe-146">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a11fe-147">開始-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a11fe-147">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a11fe-148">AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a11fe-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a11fe-149">AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a11fe-149">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
