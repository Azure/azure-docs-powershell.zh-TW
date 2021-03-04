---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: e54823cc6dff1f58b594604841c1d37bf249b7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907698"
---
# <span data-ttu-id="58efb-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="58efb-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="58efb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58efb-102">SYNOPSIS</span></span>
<span data-ttu-id="58efb-103">在資料流程的 Debug 會話中啟動 Debug 動作。</span><span class="sxs-lookup"><span data-stu-id="58efb-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="58efb-104">語法</span><span class="sxs-lookup"><span data-stu-id="58efb-104">SYNTAX</span></span>

### <span data-ttu-id="58efb-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="58efb-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58efb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="58efb-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58efb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58efb-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58efb-108">描述</span><span class="sxs-lookup"><span data-stu-id="58efb-108">DESCRIPTION</span></span>
<span data-ttu-id="58efb-109">此命令會針對在 Debug 會話中不同資料流程執行資料預覽/統計資料預覽/運算式預覽。</span><span class="sxs-lookup"><span data-stu-id="58efb-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="58efb-110">資料流程的工作流程的 PowerShell 命令順序應該是：</span><span class="sxs-lookup"><span data-stu-id="58efb-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="58efb-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="58efb-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="58efb-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="58efb-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="58efb-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (不同命令/目標重複此步驟，或重複步驟 2-3，以變更封裝) </span><span class="sxs-lookup"><span data-stu-id="58efb-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="58efb-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="58efb-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="58efb-115">例子</span><span class="sxs-lookup"><span data-stu-id="58efb-115">EXAMPLES</span></span>

### <span data-ttu-id="58efb-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="58efb-116">Example 1</span></span>
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

<span data-ttu-id="58efb-117">此範例會呼叫資料工廠 "WiKiADF" 中 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" 的 Debug 會話資料預覽命令，然後將 JSON 輸出轉換為可讀字串。</span><span class="sxs-lookup"><span data-stu-id="58efb-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="58efb-118">參數</span><span class="sxs-lookup"><span data-stu-id="58efb-118">PARAMETERS</span></span>

### <span data-ttu-id="58efb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58efb-119">-AsJob</span></span>
<span data-ttu-id="58efb-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58efb-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58efb-121">-欄</span><span class="sxs-lookup"><span data-stu-id="58efb-121">-Columns</span></span>
<span data-ttu-id="58efb-122">資料流程程統計預覽的欄清單。</span><span class="sxs-lookup"><span data-stu-id="58efb-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="58efb-123">-命令</span><span class="sxs-lookup"><span data-stu-id="58efb-123">-Command</span></span>
<span data-ttu-id="58efb-124">資料流程的 Debug 命令。</span><span class="sxs-lookup"><span data-stu-id="58efb-124">The data flow debug command.</span></span> <span data-ttu-id="58efb-125">選擇性為 executePreviewQuery、executeStatisticsQuery 和 executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="58efb-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="58efb-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="58efb-126">-DataFactory</span></span>
<span data-ttu-id="58efb-127">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="58efb-127">The data factory object.</span></span>

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

### <span data-ttu-id="58efb-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58efb-128">-DataFactoryName</span></span>
<span data-ttu-id="58efb-129">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="58efb-129">The data factory name.</span></span>

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

### <span data-ttu-id="58efb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58efb-130">-DefaultProfile</span></span>
<span data-ttu-id="58efb-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58efb-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58efb-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="58efb-132">-Expression</span></span>
<span data-ttu-id="58efb-133">資料流程運算式預覽的運算式。</span><span class="sxs-lookup"><span data-stu-id="58efb-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="58efb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58efb-134">-ResourceGroupName</span></span>
<span data-ttu-id="58efb-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="58efb-135">The resource group name.</span></span>

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

### <span data-ttu-id="58efb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58efb-136">-ResourceId</span></span>
<span data-ttu-id="58efb-137">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="58efb-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="58efb-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="58efb-138">-RowLimits</span></span>
<span data-ttu-id="58efb-139">資料流程資料預覽的列限制。</span><span class="sxs-lookup"><span data-stu-id="58efb-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="58efb-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="58efb-140">-SessionId</span></span>
<span data-ttu-id="58efb-141">資料流程的 Debug 會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="58efb-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="58efb-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="58efb-142">-StreamName</span></span>
<span data-ttu-id="58efb-143">用於進行工作流程的資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="58efb-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="58efb-144">-確認</span><span class="sxs-lookup"><span data-stu-id="58efb-144">-Confirm</span></span>
<span data-ttu-id="58efb-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58efb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58efb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58efb-146">-WhatIf</span></span>
<span data-ttu-id="58efb-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58efb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58efb-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58efb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58efb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58efb-149">CommonParameters</span></span>
<span data-ttu-id="58efb-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58efb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58efb-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58efb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58efb-152">輸入</span><span class="sxs-lookup"><span data-stu-id="58efb-152">INPUTS</span></span>

### <span data-ttu-id="58efb-153">System.String</span><span class="sxs-lookup"><span data-stu-id="58efb-153">System.String</span></span>

### <span data-ttu-id="58efb-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="58efb-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="58efb-155">輸出</span><span class="sxs-lookup"><span data-stu-id="58efb-155">OUTPUTS</span></span>

### <span data-ttu-id="58efb-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDFlowDecommessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="58efb-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="58efb-157">筆記</span><span class="sxs-lookup"><span data-stu-id="58efb-157">NOTES</span></span>
<span data-ttu-id="58efb-158">關鍵字：azure、azurerm、arm、resource、management、manager、data、keyKeywords：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="58efb-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="58efb-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="58efb-159">RELATED LINKS</span></span>

[<span data-ttu-id="58efb-160">Start-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="58efb-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="58efb-161">Get-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="58efb-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="58efb-162">Add-AzDataFactoryV2DataFlowDemediaSessionPackage</span><span class="sxs-lookup"><span data-stu-id="58efb-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="58efb-163">Stop-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="58efb-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
