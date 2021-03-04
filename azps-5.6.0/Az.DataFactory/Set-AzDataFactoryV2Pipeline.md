---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b059e48eda6367459bd90bd7ccdf93ea14387ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905153"
---
# <span data-ttu-id="5c2fa-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5c2fa-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="5c2fa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2fa-103">在 Data Factory 中建立管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="5c2fa-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c2fa-104">SYNTAX</span></span>

### <span data-ttu-id="5c2fa-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5c2fa-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c2fa-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c2fa-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c2fa-107">描述</span><span class="sxs-lookup"><span data-stu-id="5c2fa-107">DESCRIPTION</span></span>
<span data-ttu-id="5c2fa-108">Cmdlet Set-AzDataFactoryV2Pipeline Azure Data Factory 中建立管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="5c2fa-109">如果您為已存在的管線指定名稱，Cmdlet 會先提示您確認，然後再取代管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="5c2fa-110">如果您指定 Force 參數，Cmdlet 會取代現有的管線，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="5c2fa-111">請以下列循序執行這些作業：建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="5c2fa-112">-- 建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-112">-- Create linked services.</span></span>
<span data-ttu-id="5c2fa-113">-- 建立資料集。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-113">-- Create datasets.</span></span>
<span data-ttu-id="5c2fa-114">-- 建立管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-114">-- Create a pipeline.</span></span>
<span data-ttu-id="5c2fa-115">如果資料工廠中已存在相同名稱的管線，此 Cmdlet 會提示您確認是否要使用新的管線覆寫現有的管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="5c2fa-116">如果您確認覆寫現有的管線，也會取代管線定義。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="5c2fa-117">例子</span><span class="sxs-lookup"><span data-stu-id="5c2fa-117">EXAMPLES</span></span>

### <span data-ttu-id="5c2fa-118">範例 1：建立管線</span><span class="sxs-lookup"><span data-stu-id="5c2fa-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="5c2fa-119">此命令在名為 ADF 的資料工廠中建立名為DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="5c2fa-120">命令會依據檔案中DPWikisample.js的資訊。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="5c2fa-121">此檔案包含有關活動的資訊，例如管線中的複製活動和 HDInsight 活動。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="5c2fa-122">參數</span><span class="sxs-lookup"><span data-stu-id="5c2fa-122">PARAMETERS</span></span>

### <span data-ttu-id="5c2fa-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5c2fa-123">-DataFactoryName</span></span>
<span data-ttu-id="5c2fa-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5c2fa-125">此 Cmdlet 會為此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c2fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2fa-126">-DefaultProfile</span></span>
<span data-ttu-id="5c2fa-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c2fa-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5c2fa-128">-DefinitionFile</span></span>
<span data-ttu-id="5c2fa-129">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-129">The JSON file path.</span></span>

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

### <span data-ttu-id="5c2fa-130">-強制</span><span class="sxs-lookup"><span data-stu-id="5c2fa-130">-Force</span></span>
<span data-ttu-id="5c2fa-131">表示此 Cmdlet 會取代現有的管線，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="5c2fa-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c2fa-132">-Name</span></span>
<span data-ttu-id="5c2fa-133">指定要建立管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="5c2fa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2fa-134">-ResourceGroupName</span></span>
<span data-ttu-id="5c2fa-135">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5c2fa-136">此 Cmdlet 會為此參數指定的群組建立管線。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c2fa-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c2fa-137">-ResourceId</span></span>
<span data-ttu-id="5c2fa-138">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5c2fa-139">-確認</span><span class="sxs-lookup"><span data-stu-id="5c2fa-139">-Confirm</span></span>
<span data-ttu-id="5c2fa-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c2fa-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c2fa-141">-WhatIf</span></span>
<span data-ttu-id="5c2fa-142">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5c2fa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2fa-143">CommonParameters</span></span>
<span data-ttu-id="5c2fa-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2fa-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5c2fa-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2fa-146">輸入</span><span class="sxs-lookup"><span data-stu-id="5c2fa-146">INPUTS</span></span>

### <span data-ttu-id="5c2fa-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5c2fa-147">System.String</span></span>

## <span data-ttu-id="5c2fa-148">輸出</span><span class="sxs-lookup"><span data-stu-id="5c2fa-148">OUTPUTS</span></span>

### <span data-ttu-id="5c2fa-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5c2fa-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="5c2fa-150">筆記</span><span class="sxs-lookup"><span data-stu-id="5c2fa-150">NOTES</span></span>
<span data-ttu-id="5c2fa-151">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="5c2fa-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5c2fa-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c2fa-152">RELATED LINKS</span></span>

[<span data-ttu-id="5c2fa-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5c2fa-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5c2fa-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5c2fa-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5c2fa-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5c2fa-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
