---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625520"
---
# <span data-ttu-id="e3340-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e3340-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e3340-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3340-102">SYNOPSIS</span></span>
  <span data-ttu-id="e3340-103">調用管線以啟動它的執行。</span><span class="sxs-lookup"><span data-stu-id="e3340-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3340-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3340-104">SYNTAX</span></span>

### <span data-ttu-id="e3340-105">ByFactoryNameByParameterFile (預設) </span><span class="sxs-lookup"><span data-stu-id="e3340-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e3340-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3340-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e3340-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3340-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e3340-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3340-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e3340-109">說明</span><span class="sxs-lookup"><span data-stu-id="e3340-109">DESCRIPTION</span></span>
<span data-ttu-id="e3340-110">**Invoke AzureRmDataFactoryV2Pipeline** 命令會在指定的管線上啟動執行，並傳回該執行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3340-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="e3340-111">此 GUID 可以傳送至 **AzureRmDataFactoryV2PipelineRun** 或 **AzureRmDataFactoryV2ActivityRun** ，以取得此執行的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e3340-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="e3340-112">示例</span><span class="sxs-lookup"><span data-stu-id="e3340-112">EXAMPLES</span></span>

### <span data-ttu-id="e3340-113">範例1：喚醒呼叫管線以開始執行</span><span class="sxs-lookup"><span data-stu-id="e3340-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="e3340-114">這個命令會在「WikiADF」工廠中啟動「DPWikisample」管線的執行。</span><span class="sxs-lookup"><span data-stu-id="e3340-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="e3340-115">參數</span><span class="sxs-lookup"><span data-stu-id="e3340-115">PARAMETERS</span></span>

### <span data-ttu-id="e3340-116">-確認</span><span class="sxs-lookup"><span data-stu-id="e3340-116">-Confirm</span></span>
<span data-ttu-id="e3340-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3340-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3340-118">-DataFactoryName</span></span>
<span data-ttu-id="e3340-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e3340-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3340-120">-ParameterFile</span></span>
<span data-ttu-id="e3340-121">含有管線執行參數的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e3340-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-122">-參數</span><span class="sxs-lookup"><span data-stu-id="e3340-122">-Parameter</span></span>
<span data-ttu-id="e3340-123">管線執行的參數。</span><span class="sxs-lookup"><span data-stu-id="e3340-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3340-124">-InputObject</span></span>
<span data-ttu-id="e3340-125">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="e3340-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="e3340-126">-PipelineName</span></span>
<span data-ttu-id="e3340-127">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="e3340-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3340-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3340-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3340-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3340-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3340-130">-WhatIf</span></span>
<span data-ttu-id="e3340-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3340-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e3340-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e3340-132">INPUTS</span></span>

### <span data-ttu-id="e3340-133">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e3340-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="e3340-134">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3340-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="e3340-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e3340-135">OUTPUTS</span></span>

### <span data-ttu-id="e3340-136">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e3340-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="e3340-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e3340-137">NOTES</span></span>

## <span data-ttu-id="e3340-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3340-138">RELATED LINKS</span></span>
[<span data-ttu-id="e3340-139">AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e3340-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="e3340-140">AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e3340-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

