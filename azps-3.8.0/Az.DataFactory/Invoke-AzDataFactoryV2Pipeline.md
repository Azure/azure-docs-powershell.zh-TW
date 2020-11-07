---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 87d4cfadd183a6aa2652b86336b4dc8d089936fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798893"
---
# <span data-ttu-id="acca5-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="acca5-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="acca5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acca5-102">SYNOPSIS</span></span>
  <span data-ttu-id="acca5-103">調用管線以啟動它的執行。</span><span class="sxs-lookup"><span data-stu-id="acca5-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="acca5-104">句法</span><span class="sxs-lookup"><span data-stu-id="acca5-104">SYNTAX</span></span>

### <span data-ttu-id="acca5-105">ByFactoryNameByParameterFile (預設) </span><span class="sxs-lookup"><span data-stu-id="acca5-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acca5-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="acca5-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acca5-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="acca5-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acca5-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="acca5-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acca5-109">說明</span><span class="sxs-lookup"><span data-stu-id="acca5-109">DESCRIPTION</span></span>
<span data-ttu-id="acca5-110">**Invoke AzDataFactoryV2Pipeline** 命令會在指定的管線上啟動執行，並傳回該執行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="acca5-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="acca5-111">此 GUID 可以傳送至 **AzDataFactoryV2PipelineRun** 或 **AzDataFactoryV2ActivityRun** ，以取得此執行的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acca5-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="acca5-112">示例</span><span class="sxs-lookup"><span data-stu-id="acca5-112">EXAMPLES</span></span>

### <span data-ttu-id="acca5-113">範例1：喚醒呼叫管線以開始執行</span><span class="sxs-lookup"><span data-stu-id="acca5-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="acca5-114">這個命令會在「WikiADF」工廠中啟動「DPWikisample」管線的執行。</span><span class="sxs-lookup"><span data-stu-id="acca5-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="acca5-115">參數</span><span class="sxs-lookup"><span data-stu-id="acca5-115">PARAMETERS</span></span>

### <span data-ttu-id="acca5-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="acca5-116">-DataFactoryName</span></span>
<span data-ttu-id="acca5-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="acca5-117">The data factory name.</span></span>

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

### <span data-ttu-id="acca5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acca5-118">-DefaultProfile</span></span>
<span data-ttu-id="acca5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acca5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acca5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acca5-120">-InputObject</span></span>
<span data-ttu-id="acca5-121">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="acca5-121">The data factory object.</span></span>

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

### <span data-ttu-id="acca5-122">-參數</span><span class="sxs-lookup"><span data-stu-id="acca5-122">-Parameter</span></span>
<span data-ttu-id="acca5-123">管線執行的參數。</span><span class="sxs-lookup"><span data-stu-id="acca5-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="acca5-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="acca5-124">-ParameterFile</span></span>
<span data-ttu-id="acca5-125">含有管線執行參數的檔案名。</span><span class="sxs-lookup"><span data-stu-id="acca5-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="acca5-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="acca5-126">-PipelineName</span></span>
<span data-ttu-id="acca5-127">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="acca5-127">The pipeline name.</span></span>

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

### <span data-ttu-id="acca5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acca5-128">-ResourceGroupName</span></span>
<span data-ttu-id="acca5-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="acca5-129">The resource group name.</span></span>

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

### <span data-ttu-id="acca5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="acca5-130">-Confirm</span></span>
<span data-ttu-id="acca5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acca5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acca5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acca5-132">-WhatIf</span></span>
<span data-ttu-id="acca5-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acca5-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="acca5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acca5-134">CommonParameters</span></span>
<span data-ttu-id="acca5-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acca5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acca5-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acca5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acca5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="acca5-137">INPUTS</span></span>

### <span data-ttu-id="acca5-138">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="acca5-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="acca5-139">System.object</span><span class="sxs-lookup"><span data-stu-id="acca5-139">System.String</span></span>

### <span data-ttu-id="acca5-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="acca5-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acca5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="acca5-141">OUTPUTS</span></span>

### <span data-ttu-id="acca5-142">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="acca5-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="acca5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="acca5-143">NOTES</span></span>

## <span data-ttu-id="acca5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="acca5-144">RELATED LINKS</span></span>

[<span data-ttu-id="acca5-145">AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="acca5-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="acca5-146">AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="acca5-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

