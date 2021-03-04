---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: be94460a2296874acefab3232f4a73d394a523d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905150"
---
# <span data-ttu-id="5643c-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5643c-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="5643c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5643c-102">SYNOPSIS</span></span>
<span data-ttu-id="5643c-103">在 Azure Data Factory 中啟動資料流程的 Debug 會話</span><span class="sxs-lookup"><span data-stu-id="5643c-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="5643c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5643c-104">SYNTAX</span></span>

### <span data-ttu-id="5643c-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5643c-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5643c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5643c-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5643c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5643c-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5643c-108">描述</span><span class="sxs-lookup"><span data-stu-id="5643c-108">DESCRIPTION</span></span>
<span data-ttu-id="5643c-109">這個長時間執行的命令會針對即將開始的 Debug 命令啟動資料流程的 Debug 會話。</span><span class="sxs-lookup"><span data-stu-id="5643c-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="5643c-110">此命令可以附加整合執行時間定義，以設定 Debug 會話組的大小/類型。</span><span class="sxs-lookup"><span data-stu-id="5643c-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="5643c-111">資料流程的工作流程的 PowerShell 命令順序應該是：</span><span class="sxs-lookup"><span data-stu-id="5643c-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="5643c-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5643c-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="5643c-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="5643c-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="5643c-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (不同命令/目標重複此步驟，或重複步驟 2-3，以變更封裝) </span><span class="sxs-lookup"><span data-stu-id="5643c-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="5643c-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5643c-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="5643c-116">例子</span><span class="sxs-lookup"><span data-stu-id="5643c-116">EXAMPLES</span></span>

### <span data-ttu-id="5643c-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="5643c-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="5643c-118">以 AsJob 標號啟動一個 Debug 會話。</span><span class="sxs-lookup"><span data-stu-id="5643c-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="5643c-119">參數</span><span class="sxs-lookup"><span data-stu-id="5643c-119">PARAMETERS</span></span>

### <span data-ttu-id="5643c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5643c-120">-AsJob</span></span>
<span data-ttu-id="5643c-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5643c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5643c-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5643c-122">-DataFactory</span></span>
<span data-ttu-id="5643c-123">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="5643c-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5643c-124">-DataFactoryName</span></span>
<span data-ttu-id="5643c-125">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="5643c-125">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5643c-126">-DefaultProfile</span></span>
<span data-ttu-id="5643c-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5643c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5643c-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="5643c-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="5643c-129">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5643c-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5643c-130">-ResourceGroupName</span></span>
<span data-ttu-id="5643c-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5643c-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5643c-132">-ResourceId</span></span>
<span data-ttu-id="5643c-133">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5643c-133">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5643c-134">-Confirm</span></span>
<span data-ttu-id="5643c-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5643c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5643c-136">-WhatIf</span></span>
<span data-ttu-id="5643c-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5643c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5643c-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5643c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5643c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5643c-139">CommonParameters</span></span>
<span data-ttu-id="5643c-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5643c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5643c-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5643c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5643c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5643c-142">INPUTS</span></span>

### <span data-ttu-id="5643c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5643c-143">System.String</span></span>

### <span data-ttu-id="5643c-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5643c-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5643c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5643c-145">OUTPUTS</span></span>

### <span data-ttu-id="5643c-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDFlowDeSession</span><span class="sxs-lookup"><span data-stu-id="5643c-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="5643c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5643c-147">NOTES</span></span>
<span data-ttu-id="5643c-148">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="5643c-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5643c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="5643c-149">RELATED LINKS</span></span>

[<span data-ttu-id="5643c-150">Get-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="5643c-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="5643c-151">Add-AzDataFactoryV2DataFlowDemediaSessionPackage</span><span class="sxs-lookup"><span data-stu-id="5643c-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="5643c-152">Invoke-AzDataFactoryV2DataFlowDemediaSessionCommand</span><span class="sxs-lookup"><span data-stu-id="5643c-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="5643c-153">Stop-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="5643c-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)