---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: a8e75d6ef44453891660a7d5d35216dace346cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907694"
---
# <span data-ttu-id="8972b-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8972b-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8972b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8972b-102">SYNOPSIS</span></span>
  <span data-ttu-id="8972b-103">會啟動管線以開始執行。</span><span class="sxs-lookup"><span data-stu-id="8972b-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="8972b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8972b-104">SYNTAX</span></span>

### <span data-ttu-id="8972b-105">ByFactoryNameByParameterFile (預設) </span><span class="sxs-lookup"><span data-stu-id="8972b-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8972b-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="8972b-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8972b-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="8972b-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8972b-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="8972b-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8972b-109">描述</span><span class="sxs-lookup"><span data-stu-id="8972b-109">DESCRIPTION</span></span>
<span data-ttu-id="8972b-110">**Invoke-AzDataFactoryV2Pipeline 命令** 會啟動指定管線上的執行，並針對該執行過程返回識別碼。</span><span class="sxs-lookup"><span data-stu-id="8972b-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="8972b-111">此 GUID 可以傳遞至 **Get-AzDataFactoryV2PipelineRun** 或 **Get-AzDataFactoryV2ActivityRun，** 以取得有關此執行的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8972b-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="8972b-112">例子</span><span class="sxs-lookup"><span data-stu-id="8972b-112">EXAMPLES</span></span>

### <span data-ttu-id="8972b-113">範例 1：在管道中啟動執行</span><span class="sxs-lookup"><span data-stu-id="8972b-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="8972b-114">此命令會啟動「WikiADF」工廠中「DPWikisample」管線的執行程式。</span><span class="sxs-lookup"><span data-stu-id="8972b-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="8972b-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="8972b-115">Example 2</span></span>

<span data-ttu-id="8972b-116">會啟動管線以開始執行。</span><span class="sxs-lookup"><span data-stu-id="8972b-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="8972b-117"> (自動) </span><span class="sxs-lookup"><span data-stu-id="8972b-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="8972b-118">參數</span><span class="sxs-lookup"><span data-stu-id="8972b-118">PARAMETERS</span></span>

### <span data-ttu-id="8972b-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8972b-119">-DataFactoryName</span></span>
<span data-ttu-id="8972b-120">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="8972b-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8972b-121">-DefaultProfile</span></span>
<span data-ttu-id="8972b-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8972b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8972b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8972b-123">-InputObject</span></span>
<span data-ttu-id="8972b-124">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="8972b-124">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="8972b-125">-IsRecovery</span></span>
<span data-ttu-id="8972b-126">復原模式標標。</span><span class="sxs-lookup"><span data-stu-id="8972b-126">Recovery mode flag.</span></span> <span data-ttu-id="8972b-127">如果復原模式設為 True，則指定的參照管線執行與新執行會在同一個 groupId 下分組。</span><span class="sxs-lookup"><span data-stu-id="8972b-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8972b-128">-Parameter</span></span>
<span data-ttu-id="8972b-129">管線執行的參數。</span><span class="sxs-lookup"><span data-stu-id="8972b-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="8972b-130">-ParameterFile</span></span>
<span data-ttu-id="8972b-131">具有管線執行參數的檔案名。</span><span class="sxs-lookup"><span data-stu-id="8972b-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8972b-132">-PipelineName</span></span>
<span data-ttu-id="8972b-133">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="8972b-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="8972b-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="8972b-135">要重新執行的管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="8972b-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="8972b-136">如果指定執行識別碼，將會使用指定執行的參數來建立新執行。</span><span class="sxs-lookup"><span data-stu-id="8972b-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8972b-137">-ResourceGroupName</span></span>
<span data-ttu-id="8972b-138">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8972b-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="8972b-139">-StartActivityName</span></span>
<span data-ttu-id="8972b-140">在復原模式中，重新執行會從此活動開始。</span><span class="sxs-lookup"><span data-stu-id="8972b-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="8972b-141">如果未指定，將會執行所有活動。</span><span class="sxs-lookup"><span data-stu-id="8972b-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="8972b-142">-StartFromFailure</span></span>
<span data-ttu-id="8972b-143">從失敗的活動標標開始重新執行。</span><span class="sxs-lookup"><span data-stu-id="8972b-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="8972b-144">在復原模式中，如果指定，重新執行會從失敗的活動開始。</span><span class="sxs-lookup"><span data-stu-id="8972b-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8972b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="8972b-145">-Confirm</span></span>
<span data-ttu-id="8972b-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8972b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8972b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8972b-147">-WhatIf</span></span>
<span data-ttu-id="8972b-148">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8972b-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8972b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8972b-149">CommonParameters</span></span>
<span data-ttu-id="8972b-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8972b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8972b-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8972b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8972b-152">輸入</span><span class="sxs-lookup"><span data-stu-id="8972b-152">INPUTS</span></span>

### <span data-ttu-id="8972b-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8972b-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="8972b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8972b-154">System.String</span></span>

### <span data-ttu-id="8972b-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8972b-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8972b-156">輸出</span><span class="sxs-lookup"><span data-stu-id="8972b-156">OUTPUTS</span></span>

### <span data-ttu-id="8972b-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8972b-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="8972b-158">筆記</span><span class="sxs-lookup"><span data-stu-id="8972b-158">NOTES</span></span>

## <span data-ttu-id="8972b-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="8972b-159">RELATED LINKS</span></span>

[<span data-ttu-id="8972b-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8972b-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="8972b-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="8972b-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

