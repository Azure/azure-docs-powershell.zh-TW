---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454924"
---
# <span data-ttu-id="e01af-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e01af-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="e01af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e01af-102">SYNOPSIS</span></span>
<span data-ttu-id="e01af-103">在自動化中停止 DSC 節點配置部署。</span><span class="sxs-lookup"><span data-stu-id="e01af-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="e01af-104">它只會停止目前的部署作業，但不會取消指派已指派的節點配置。</span><span class="sxs-lookup"><span data-stu-id="e01af-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e01af-105">句法</span><span class="sxs-lookup"><span data-stu-id="e01af-105">SYNTAX</span></span>

### <span data-ttu-id="e01af-106">ByJobId (預設) </span><span class="sxs-lookup"><span data-stu-id="e01af-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e01af-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="e01af-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e01af-108">說明</span><span class="sxs-lookup"><span data-stu-id="e01af-108">DESCRIPTION</span></span>
<span data-ttu-id="e01af-109">**Stop-AzureRmAutomationDscNodeConfigurationDeployment** Cmdlet 會在 Azure 自動化中停止部署所需的狀態設定 (DSC) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="e01af-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="e01af-110">它會停止將節點配置指派給節點群組（如果有剩餘的指派），但不會取消指派已指派的節點。</span><span class="sxs-lookup"><span data-stu-id="e01af-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="e01af-111">若要登出排程作業，請在 JobScheduleId 中使用 [ [取消註冊] AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) ，以取消指派現有的排程作業。</span><span class="sxs-lookup"><span data-stu-id="e01af-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="e01af-112">示例</span><span class="sxs-lookup"><span data-stu-id="e01af-112">EXAMPLES</span></span>

### <span data-ttu-id="e01af-113">範例1：在自動化中部署 Azure DSC 節點配置</span><span class="sxs-lookup"><span data-stu-id="e01af-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e01af-114">上述命令會停止與已傳入作業 Id 的 DSC 節點配置部署作業。</span><span class="sxs-lookup"><span data-stu-id="e01af-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="e01af-115">參數</span><span class="sxs-lookup"><span data-stu-id="e01af-115">PARAMETERS</span></span>

### <span data-ttu-id="e01af-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e01af-116">-AutomationAccountName</span></span>
<span data-ttu-id="e01af-117">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e01af-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e01af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01af-118">-ResourceGroupName</span></span>
<span data-ttu-id="e01af-119">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e01af-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="e01af-120">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="e01af-120">-JobId</span></span>
<span data-ttu-id="e01af-121">指定現有部署作業的作業 id。</span><span class="sxs-lookup"><span data-stu-id="e01af-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="e01af-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e01af-122">-PassThru</span></span>
<span data-ttu-id="e01af-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e01af-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e01af-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e01af-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e01af-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e01af-125">-Force</span></span>
<span data-ttu-id="e01af-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="e01af-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e01af-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e01af-127">-Confirm</span></span>
<span data-ttu-id="e01af-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e01af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e01af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e01af-129">-WhatIf</span></span>
<span data-ttu-id="e01af-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e01af-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e01af-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e01af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e01af-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01af-132">-DefaultProfile</span></span>
<span data-ttu-id="e01af-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e01af-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e01af-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e01af-134">-InputObject</span></span>
<span data-ttu-id="e01af-135">[管道] 的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e01af-135">Input object for Piping.</span></span>

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

### <span data-ttu-id="e01af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01af-136">CommonParameters</span></span>
<span data-ttu-id="e01af-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e01af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01af-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e01af-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01af-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e01af-139">INPUTS</span></span>

## <span data-ttu-id="e01af-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e01af-140">OUTPUTS</span></span>

## <span data-ttu-id="e01af-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e01af-141">NOTES</span></span>

## <span data-ttu-id="e01af-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e01af-142">RELATED LINKS</span></span>

[<span data-ttu-id="e01af-143">開始-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e01af-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="e01af-144">匯入-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e01af-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="e01af-145">開始-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e01af-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e01af-146">AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e01af-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e01af-147">AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="e01af-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
