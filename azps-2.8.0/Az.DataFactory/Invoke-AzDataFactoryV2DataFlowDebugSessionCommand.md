---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 45419ede425b5d5ea3ba9fcbbbfb024fe8ba9358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612982"
---
# <span data-ttu-id="d49cd-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="d49cd-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="d49cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d49cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d49cd-103">在資料流程調試會話中呼叫調試動作。</span><span class="sxs-lookup"><span data-stu-id="d49cd-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="d49cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="d49cd-104">SYNTAX</span></span>

### <span data-ttu-id="d49cd-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d49cd-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d49cd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d49cd-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d49cd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d49cd-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d49cd-108">說明</span><span class="sxs-lookup"><span data-stu-id="d49cd-108">DESCRIPTION</span></span>
<span data-ttu-id="d49cd-109">這個命令會針對調試會話中不同的資料流程資料流程執行資料預覽/統計預覽/運算式預覽。</span><span class="sxs-lookup"><span data-stu-id="d49cd-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="d49cd-110">資料流程調試工作流程的 PowerShell 命令順序應該是：</span><span class="sxs-lookup"><span data-stu-id="d49cd-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="d49cd-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d49cd-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="d49cd-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="d49cd-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="d49cd-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (針對不同的命令/目標重複這個步驟，或重複步驟2-3 來變更套件檔案) </span><span class="sxs-lookup"><span data-stu-id="d49cd-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="d49cd-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d49cd-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="d49cd-115">示例</span><span class="sxs-lookup"><span data-stu-id="d49cd-115">EXAMPLES</span></span>

### <span data-ttu-id="d49cd-116">範例1</span><span class="sxs-lookup"><span data-stu-id="d49cd-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="d49cd-117">這個範例會在資料工廠 "WiKiADF" 中，針對調試會話 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" 調用資料預覽命令，然後將 JSON 輸出轉換成可讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="d49cd-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="d49cd-118">參數</span><span class="sxs-lookup"><span data-stu-id="d49cd-118">PARAMETERS</span></span>

### <span data-ttu-id="d49cd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d49cd-119">-AsJob</span></span>
<span data-ttu-id="d49cd-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d49cd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d49cd-121">-欄</span><span class="sxs-lookup"><span data-stu-id="d49cd-121">-Columns</span></span>
<span data-ttu-id="d49cd-122">[資料流程程統計資料預覽] 的 [欄] 清單。</span><span class="sxs-lookup"><span data-stu-id="d49cd-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cd-123">-Command</span><span class="sxs-lookup"><span data-stu-id="d49cd-123">-Command</span></span>
<span data-ttu-id="d49cd-124">[資料流程程調試] 命令。</span><span class="sxs-lookup"><span data-stu-id="d49cd-124">The data flow debug command.</span></span> <span data-ttu-id="d49cd-125">Optionals 是 executePreviewQuery、executeStatisticsQuery 和 executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="d49cd-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cd-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d49cd-126">-DataFactory</span></span>
<span data-ttu-id="d49cd-127">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="d49cd-127">The data factory object.</span></span>

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

### <span data-ttu-id="d49cd-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d49cd-128">-DataFactoryName</span></span>
<span data-ttu-id="d49cd-129">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d49cd-129">The data factory name.</span></span>

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

### <span data-ttu-id="d49cd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49cd-130">-DefaultProfile</span></span>
<span data-ttu-id="d49cd-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d49cd-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d49cd-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="d49cd-132">-Expression</span></span>
<span data-ttu-id="d49cd-133">資料流程程運算式預覽的運算式。</span><span class="sxs-lookup"><span data-stu-id="d49cd-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49cd-134">-ResourceGroupName</span></span>
<span data-ttu-id="d49cd-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d49cd-135">The resource group name.</span></span>

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

### <span data-ttu-id="d49cd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d49cd-136">-ResourceId</span></span>
<span data-ttu-id="d49cd-137">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d49cd-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d49cd-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="d49cd-138">-RowLimits</span></span>
<span data-ttu-id="d49cd-139">資料流程程資料預覽的列限制。</span><span class="sxs-lookup"><span data-stu-id="d49cd-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cd-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="d49cd-140">-SessionId</span></span>
<span data-ttu-id="d49cd-141">資料流程調試會話 ID。</span><span class="sxs-lookup"><span data-stu-id="d49cd-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cd-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="d49cd-142">-StreamName</span></span>
<span data-ttu-id="d49cd-143">資料流程的資料流程名稱以進行調試。</span><span class="sxs-lookup"><span data-stu-id="d49cd-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cd-144">-確認</span><span class="sxs-lookup"><span data-stu-id="d49cd-144">-Confirm</span></span>
<span data-ttu-id="d49cd-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d49cd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d49cd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49cd-146">-WhatIf</span></span>
<span data-ttu-id="d49cd-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d49cd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d49cd-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d49cd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d49cd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49cd-149">CommonParameters</span></span>
<span data-ttu-id="d49cd-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d49cd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49cd-151">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d49cd-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49cd-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d49cd-152">INPUTS</span></span>

### <span data-ttu-id="d49cd-153">System.object</span><span class="sxs-lookup"><span data-stu-id="d49cd-153">System.String</span></span>

### <span data-ttu-id="d49cd-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d49cd-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d49cd-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d49cd-155">OUTPUTS</span></span>

### <span data-ttu-id="d49cd-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="d49cd-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="d49cd-157">筆記</span><span class="sxs-lookup"><span data-stu-id="d49cd-157">NOTES</span></span>
<span data-ttu-id="d49cd-158">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，factoriesKeywords： azure，azurerm，data，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="d49cd-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d49cd-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="d49cd-159">RELATED LINKS</span></span>

[<span data-ttu-id="d49cd-160">開始-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d49cd-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d49cd-161">AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d49cd-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d49cd-162">附加 AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="d49cd-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="d49cd-163">停止 AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d49cd-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
