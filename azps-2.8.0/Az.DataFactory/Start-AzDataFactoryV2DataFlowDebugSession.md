---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 98b34b4926dc4edc15d30308b2d6bfee33336f0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612903"
---
# <span data-ttu-id="5f227-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5f227-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="5f227-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f227-102">SYNOPSIS</span></span>
<span data-ttu-id="5f227-103">在 Azure 資料工廠中啟動資料流程調試會話</span><span class="sxs-lookup"><span data-stu-id="5f227-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="5f227-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f227-104">SYNTAX</span></span>

### <span data-ttu-id="5f227-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5f227-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f227-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5f227-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f227-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f227-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f227-108">說明</span><span class="sxs-lookup"><span data-stu-id="5f227-108">DESCRIPTION</span></span>
<span data-ttu-id="5f227-109">這個長時間執行命令會啟動近期調試命令的資料資料流程調試會話。</span><span class="sxs-lookup"><span data-stu-id="5f227-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="5f227-110">這個命令可以附加整合執行時間定義來設定調試會話群集的大小/類型。</span><span class="sxs-lookup"><span data-stu-id="5f227-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="5f227-111">資料流程調試工作流程的 PowerShell 命令順序應該是：</span><span class="sxs-lookup"><span data-stu-id="5f227-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="5f227-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5f227-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="5f227-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="5f227-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="5f227-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (針對不同的命令/目標重複這個步驟，或重複步驟2-3 來變更套件檔案) </span><span class="sxs-lookup"><span data-stu-id="5f227-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="5f227-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5f227-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="5f227-116">示例</span><span class="sxs-lookup"><span data-stu-id="5f227-116">EXAMPLES</span></span>

### <span data-ttu-id="5f227-117">範例1</span><span class="sxs-lookup"><span data-stu-id="5f227-117">Example 1</span></span>
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

<span data-ttu-id="5f227-118">啟動含 AsJob 標誌的調試會話。</span><span class="sxs-lookup"><span data-stu-id="5f227-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="5f227-119">參數</span><span class="sxs-lookup"><span data-stu-id="5f227-119">PARAMETERS</span></span>

### <span data-ttu-id="5f227-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f227-120">-AsJob</span></span>
<span data-ttu-id="5f227-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5f227-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f227-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5f227-122">-DataFactory</span></span>
<span data-ttu-id="5f227-123">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="5f227-123">The data factory object.</span></span>

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

### <span data-ttu-id="5f227-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f227-124">-DataFactoryName</span></span>
<span data-ttu-id="5f227-125">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="5f227-125">The data factory name.</span></span>

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

### <span data-ttu-id="5f227-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f227-126">-DefaultProfile</span></span>
<span data-ttu-id="5f227-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f227-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f227-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="5f227-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="5f227-129">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="5f227-129">The JSON file path.</span></span>

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

### <span data-ttu-id="5f227-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f227-130">-ResourceGroupName</span></span>
<span data-ttu-id="5f227-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f227-131">The resource group name.</span></span>

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

### <span data-ttu-id="5f227-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f227-132">-ResourceId</span></span>
<span data-ttu-id="5f227-133">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f227-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5f227-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5f227-134">-Confirm</span></span>
<span data-ttu-id="5f227-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f227-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f227-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f227-136">-WhatIf</span></span>
<span data-ttu-id="5f227-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f227-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f227-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f227-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f227-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f227-139">CommonParameters</span></span>
<span data-ttu-id="5f227-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f227-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f227-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5f227-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f227-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5f227-142">INPUTS</span></span>

### <span data-ttu-id="5f227-143">System.object</span><span class="sxs-lookup"><span data-stu-id="5f227-143">System.String</span></span>

### <span data-ttu-id="5f227-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5f227-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5f227-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5f227-145">OUTPUTS</span></span>

### <span data-ttu-id="5f227-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5f227-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="5f227-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5f227-147">NOTES</span></span>
<span data-ttu-id="5f227-148">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="5f227-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5f227-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f227-149">RELATED LINKS</span></span>

[<span data-ttu-id="5f227-150">AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5f227-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="5f227-151">附加 AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="5f227-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="5f227-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="5f227-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="5f227-153">停止 AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="5f227-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)