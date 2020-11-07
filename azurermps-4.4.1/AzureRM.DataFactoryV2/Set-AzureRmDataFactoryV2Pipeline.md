---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2a936b9a75e9fc1053e2202950a6a6b4c49bd3a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626632"
---
# <span data-ttu-id="91579-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="91579-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="91579-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91579-102">SYNOPSIS</span></span>
<span data-ttu-id="91579-103">在資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="91579-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91579-104">句法</span><span class="sxs-lookup"><span data-stu-id="91579-104">SYNTAX</span></span>

### <span data-ttu-id="91579-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="91579-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91579-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91579-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="91579-107">說明</span><span class="sxs-lookup"><span data-stu-id="91579-107">DESCRIPTION</span></span>
<span data-ttu-id="91579-108">Set-AzureRmDataFactoryV2Pipeline Cmdlet 會在 Azure 資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="91579-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="91579-109">如果您為已存在的管線指定名稱，則此 Cmdlet 會在您取代管線之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91579-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="91579-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的管線，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="91579-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="91579-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="91579-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="91579-112">如果資料工廠中已經有相同名稱的管線，這個 Cmdlet 會提示您確認是否要使用新的管線覆寫現有管線。</span><span class="sxs-lookup"><span data-stu-id="91579-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="91579-113">如果您確認覆寫現有的管線，也會取代管線定義。</span><span class="sxs-lookup"><span data-stu-id="91579-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="91579-114">示例</span><span class="sxs-lookup"><span data-stu-id="91579-114">EXAMPLES</span></span>

### <span data-ttu-id="91579-115">範例1：建立管線</span><span class="sxs-lookup"><span data-stu-id="91579-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="91579-116">這個命令會在名為 [ADF] 的資料工廠中建立名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="91579-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="91579-117">該命令根據檔案中 DPWikisample.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="91579-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="91579-118">此檔案包含有關活動的資訊，例如在管線中複製活動和 HDInsight 活動。</span><span class="sxs-lookup"><span data-stu-id="91579-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="91579-119">參數</span><span class="sxs-lookup"><span data-stu-id="91579-119">PARAMETERS</span></span>

### <span data-ttu-id="91579-120">-確認</span><span class="sxs-lookup"><span data-stu-id="91579-120">-Confirm</span></span>
<span data-ttu-id="91579-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91579-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91579-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="91579-122">-DataFactoryName</span></span>
<span data-ttu-id="91579-123">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="91579-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="91579-124">這個 Cmdlet 會針對此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="91579-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91579-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="91579-125">-DefinitionFile</span></span>
<span data-ttu-id="91579-126">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="91579-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91579-127">-Force</span><span class="sxs-lookup"><span data-stu-id="91579-127">-Force</span></span>
<span data-ttu-id="91579-128">表示此 Cmdlet 會取代現有的管線，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91579-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="91579-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="91579-129">-Name</span></span>
<span data-ttu-id="91579-130">指定要建立的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="91579-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91579-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91579-131">-ResourceGroupName</span></span>
<span data-ttu-id="91579-132">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91579-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="91579-133">這個 Cmdlet 會針對此參數指定的群組建立管線。</span><span class="sxs-lookup"><span data-stu-id="91579-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91579-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91579-134">-ResourceId</span></span>
<span data-ttu-id="91579-135">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="91579-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91579-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91579-136">-WhatIf</span></span>
<span data-ttu-id="91579-137">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91579-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="91579-138">輸入</span><span class="sxs-lookup"><span data-stu-id="91579-138">INPUTS</span></span>

### <span data-ttu-id="91579-139">System.object</span><span class="sxs-lookup"><span data-stu-id="91579-139">System.String</span></span>


## <span data-ttu-id="91579-140">輸出</span><span class="sxs-lookup"><span data-stu-id="91579-140">OUTPUTS</span></span>

### <span data-ttu-id="91579-141">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="91579-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="91579-142">筆記</span><span class="sxs-lookup"><span data-stu-id="91579-142">NOTES</span></span>
<span data-ttu-id="91579-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="91579-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="91579-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="91579-144">RELATED LINKS</span></span>
[<span data-ttu-id="91579-145">AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="91579-145">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="91579-146">移除-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="91579-146">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="91579-147">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="91579-147">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
