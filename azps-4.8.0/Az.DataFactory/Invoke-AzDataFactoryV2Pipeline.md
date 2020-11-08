---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136485"
---
# <span data-ttu-id="fe0d9-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe0d9-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="fe0d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe0d9-102">SYNOPSIS</span></span>
  <span data-ttu-id="fe0d9-103">調用管線以啟動它的執行。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="fe0d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe0d9-104">SYNTAX</span></span>

### <span data-ttu-id="fe0d9-105">ByFactoryNameByParameterFile (預設) </span><span class="sxs-lookup"><span data-stu-id="fe0d9-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0d9-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="fe0d9-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0d9-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe0d9-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0d9-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="fe0d9-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0d9-109">說明</span><span class="sxs-lookup"><span data-stu-id="fe0d9-109">DESCRIPTION</span></span>
<span data-ttu-id="fe0d9-110">**Invoke AzDataFactoryV2Pipeline** 命令會在指定的管線上啟動執行，並傳回該執行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="fe0d9-111">此 GUID 可以傳送至 **AzDataFactoryV2PipelineRun** 或 **AzDataFactoryV2ActivityRun** ，以取得此執行的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="fe0d9-112">示例</span><span class="sxs-lookup"><span data-stu-id="fe0d9-112">EXAMPLES</span></span>

### <span data-ttu-id="fe0d9-113">範例1：喚醒呼叫管線以開始執行</span><span class="sxs-lookup"><span data-stu-id="fe0d9-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="fe0d9-114">這個命令會在「WikiADF」工廠中啟動「DPWikisample」管線的執行。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="fe0d9-115">範例2</span><span class="sxs-lookup"><span data-stu-id="fe0d9-115">Example 2</span></span>

<span data-ttu-id="fe0d9-116">調用管線以啟動它的執行。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="fe0d9-117"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="fe0d9-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="fe0d9-118">參數</span><span class="sxs-lookup"><span data-stu-id="fe0d9-118">PARAMETERS</span></span>

### <span data-ttu-id="fe0d9-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fe0d9-119">-DataFactoryName</span></span>
<span data-ttu-id="fe0d9-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-120">The data factory name.</span></span>

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

### <span data-ttu-id="fe0d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0d9-121">-DefaultProfile</span></span>
<span data-ttu-id="fe0d9-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0d9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe0d9-123">-InputObject</span></span>
<span data-ttu-id="fe0d9-124">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-124">The data factory object.</span></span>

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

### <span data-ttu-id="fe0d9-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="fe0d9-125">-IsRecovery</span></span>
<span data-ttu-id="fe0d9-126">[復原模式] 旗標。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-126">Recovery mode flag.</span></span> <span data-ttu-id="fe0d9-127">如果將 [復原模式] 設定為 true，則會執行指定的參照管線，而新的執行將會群組為相同的 groupId。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="fe0d9-128">-參數</span><span class="sxs-lookup"><span data-stu-id="fe0d9-128">-Parameter</span></span>
<span data-ttu-id="fe0d9-129">管線執行的參數。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="fe0d9-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="fe0d9-130">-ParameterFile</span></span>
<span data-ttu-id="fe0d9-131">含有管線執行參數的檔案名。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="fe0d9-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="fe0d9-132">-PipelineName</span></span>
<span data-ttu-id="fe0d9-133">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-133">The pipeline name.</span></span>

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

### <span data-ttu-id="fe0d9-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="fe0d9-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="fe0d9-135">要重新執行的管線執行 ID。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="fe0d9-136">如果指定了 [執行識別碼]，則會使用指定執行的參數來建立新的執行。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="fe0d9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0d9-137">-ResourceGroupName</span></span>
<span data-ttu-id="fe0d9-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-138">The resource group name.</span></span>

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

### <span data-ttu-id="fe0d9-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="fe0d9-139">-StartActivityName</span></span>
<span data-ttu-id="fe0d9-140">在 [恢復] 模式中，[重新執行] 就會從這個活動開始。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="fe0d9-141">如果未指定，所有活動將會執行。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="fe0d9-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="fe0d9-142">-StartFromFailure</span></span>
<span data-ttu-id="fe0d9-143">從失敗的活動標誌開始重新執行。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="fe0d9-144">如果已指定，則在 [恢復] 模式中，[重新執行] 會從失敗的活動開始。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="fe0d9-145">-確認</span><span class="sxs-lookup"><span data-stu-id="fe0d9-145">-Confirm</span></span>
<span data-ttu-id="fe0d9-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0d9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0d9-147">-WhatIf</span></span>
<span data-ttu-id="fe0d9-148">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fe0d9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0d9-149">CommonParameters</span></span>
<span data-ttu-id="fe0d9-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0d9-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0d9-152">輸入</span><span class="sxs-lookup"><span data-stu-id="fe0d9-152">INPUTS</span></span>

### <span data-ttu-id="fe0d9-153">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="fe0d9-154">System.object</span><span class="sxs-lookup"><span data-stu-id="fe0d9-154">System.String</span></span>

### <span data-ttu-id="fe0d9-155">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe0d9-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe0d9-156">輸出</span><span class="sxs-lookup"><span data-stu-id="fe0d9-156">OUTPUTS</span></span>

### <span data-ttu-id="fe0d9-157">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fe0d9-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="fe0d9-158">筆記</span><span class="sxs-lookup"><span data-stu-id="fe0d9-158">NOTES</span></span>

## <span data-ttu-id="fe0d9-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe0d9-159">RELATED LINKS</span></span>

[<span data-ttu-id="fe0d9-160">AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="fe0d9-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="fe0d9-161">AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="fe0d9-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

