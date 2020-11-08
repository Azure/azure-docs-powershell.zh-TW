---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969320"
---
# <span data-ttu-id="45d17-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="45d17-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="45d17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45d17-102">SYNOPSIS</span></span>
<span data-ttu-id="45d17-103">在資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="45d17-104">句法</span><span class="sxs-lookup"><span data-stu-id="45d17-104">SYNTAX</span></span>

### <span data-ttu-id="45d17-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="45d17-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45d17-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45d17-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d17-107">說明</span><span class="sxs-lookup"><span data-stu-id="45d17-107">DESCRIPTION</span></span>
<span data-ttu-id="45d17-108">Set-AzDataFactoryV2Pipeline Cmdlet 會在 Azure 資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="45d17-109">如果您為已存在的管線指定名稱，則此 Cmdlet 會在您取代管線之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45d17-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="45d17-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的管線，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="45d17-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="45d17-111">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="45d17-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="45d17-112">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="45d17-112">-- Create linked services.</span></span>
<span data-ttu-id="45d17-113">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="45d17-113">-- Create datasets.</span></span>
<span data-ttu-id="45d17-114">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-114">-- Create a pipeline.</span></span>
<span data-ttu-id="45d17-115">如果資料工廠中已經有相同名稱的管線，這個 Cmdlet 會提示您確認是否要使用新的管線覆寫現有管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="45d17-116">如果您確認覆寫現有的管線，也會取代管線定義。</span><span class="sxs-lookup"><span data-stu-id="45d17-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="45d17-117">示例</span><span class="sxs-lookup"><span data-stu-id="45d17-117">EXAMPLES</span></span>

### <span data-ttu-id="45d17-118">範例1：建立管線</span><span class="sxs-lookup"><span data-stu-id="45d17-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="45d17-119">這個命令會在名為 [ADF] 的資料工廠中建立名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="45d17-120">該命令根據檔案中 DPWikisample.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="45d17-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="45d17-121">此檔案包含有關活動的資訊，例如在管線中複製活動和 HDInsight 活動。</span><span class="sxs-lookup"><span data-stu-id="45d17-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="45d17-122">參數</span><span class="sxs-lookup"><span data-stu-id="45d17-122">PARAMETERS</span></span>

### <span data-ttu-id="45d17-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="45d17-123">-DataFactoryName</span></span>
<span data-ttu-id="45d17-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="45d17-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="45d17-125">這個 Cmdlet 會針對此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="45d17-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d17-126">-DefaultProfile</span></span>
<span data-ttu-id="45d17-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45d17-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d17-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="45d17-128">-DefinitionFile</span></span>
<span data-ttu-id="45d17-129">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="45d17-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d17-130">-Force</span><span class="sxs-lookup"><span data-stu-id="45d17-130">-Force</span></span>
<span data-ttu-id="45d17-131">表示此 Cmdlet 會取代現有的管線，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45d17-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="45d17-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="45d17-132">-Name</span></span>
<span data-ttu-id="45d17-133">指定要建立的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="45d17-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d17-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d17-134">-ResourceGroupName</span></span>
<span data-ttu-id="45d17-135">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45d17-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="45d17-136">這個 Cmdlet 會針對此參數指定的群組建立管線。</span><span class="sxs-lookup"><span data-stu-id="45d17-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="45d17-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45d17-137">-ResourceId</span></span>
<span data-ttu-id="45d17-138">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="45d17-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="45d17-139">-確認</span><span class="sxs-lookup"><span data-stu-id="45d17-139">-Confirm</span></span>
<span data-ttu-id="45d17-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45d17-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d17-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d17-141">-WhatIf</span></span>
<span data-ttu-id="45d17-142">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45d17-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="45d17-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d17-143">CommonParameters</span></span>
<span data-ttu-id="45d17-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45d17-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d17-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45d17-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d17-146">輸入</span><span class="sxs-lookup"><span data-stu-id="45d17-146">INPUTS</span></span>

### <span data-ttu-id="45d17-147">System.object</span><span class="sxs-lookup"><span data-stu-id="45d17-147">System.String</span></span>

## <span data-ttu-id="45d17-148">輸出</span><span class="sxs-lookup"><span data-stu-id="45d17-148">OUTPUTS</span></span>

### <span data-ttu-id="45d17-149">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="45d17-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="45d17-150">筆記</span><span class="sxs-lookup"><span data-stu-id="45d17-150">NOTES</span></span>
<span data-ttu-id="45d17-151">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="45d17-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="45d17-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="45d17-152">RELATED LINKS</span></span>

[<span data-ttu-id="45d17-153">AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="45d17-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="45d17-154">移除-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="45d17-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="45d17-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="45d17-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
