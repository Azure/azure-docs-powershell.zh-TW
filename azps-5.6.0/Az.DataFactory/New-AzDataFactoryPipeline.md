---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: ad731dc612290e572ee74a967788e324f764a930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906730"
---
# <span data-ttu-id="cc000-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cc000-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="cc000-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc000-102">SYNOPSIS</span></span>
<span data-ttu-id="cc000-103">在 Data Factory 中建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="cc000-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc000-104">SYNTAX</span></span>

### <span data-ttu-id="cc000-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cc000-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc000-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cc000-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc000-107">描述</span><span class="sxs-lookup"><span data-stu-id="cc000-107">DESCRIPTION</span></span>
<span data-ttu-id="cc000-108">**New-AzDataFactoryPipeline** Cmdlet 在 Azure Data Factory 中建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="cc000-109">如果您為已存在的管線指定名稱，Cmdlet 會先提示您確認，然後再取代管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="cc000-110">如果您指定 *Force* 參數，Cmdlet 會取代現有的管線，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="cc000-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="cc000-111">請以下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="cc000-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="cc000-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc000-112">Create a data factory.</span></span> 
- <span data-ttu-id="cc000-113">建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="cc000-113">Create linked services.</span></span> 
- <span data-ttu-id="cc000-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="cc000-114">Create datasets.</span></span> 
- <span data-ttu-id="cc000-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-115">Create a pipeline.</span></span>
<span data-ttu-id="cc000-116">如果資料工廠中已存在相同名稱的管線，此 Cmdlet 會提示您確認是否要使用新的管線覆寫現有的管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="cc000-117">如果您確認覆寫現有的管線，也會取代管線定義。</span><span class="sxs-lookup"><span data-stu-id="cc000-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="cc000-118">例子</span><span class="sxs-lookup"><span data-stu-id="cc000-118">EXAMPLES</span></span>

### <span data-ttu-id="cc000-119">範例 1：建立管線</span><span class="sxs-lookup"><span data-stu-id="cc000-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="cc000-120">此命令在名為 ADF 的資料工廠中建立名為DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="cc000-121">命令會依據檔案中DPWikisample.js的資訊。</span><span class="sxs-lookup"><span data-stu-id="cc000-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="cc000-122">此檔案包含有關活動的資訊，例如管線中的複製活動和 HDInsight 活動。</span><span class="sxs-lookup"><span data-stu-id="cc000-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="cc000-123">參數</span><span class="sxs-lookup"><span data-stu-id="cc000-123">PARAMETERS</span></span>

### <span data-ttu-id="cc000-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cc000-124">-DataFactory</span></span>
<span data-ttu-id="cc000-125">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="cc000-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cc000-126">此 Cmdlet 會為此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc000-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cc000-127">-DataFactoryName</span></span>
<span data-ttu-id="cc000-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc000-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cc000-129">此 Cmdlet 會為此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc000-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc000-130">-DefaultProfile</span></span>
<span data-ttu-id="cc000-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cc000-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc000-132">-檔案</span><span class="sxs-lookup"><span data-stu-id="cc000-132">-File</span></span>
<span data-ttu-id="cc000-133">指定包含管線描述之 JSON (JSON) 之 JavaScript 物件標記法的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cc000-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="cc000-134">-強制</span><span class="sxs-lookup"><span data-stu-id="cc000-134">-Force</span></span>
<span data-ttu-id="cc000-135">表示此 Cmdlet 會取代現有的管線，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc000-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cc000-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc000-136">-Name</span></span>
<span data-ttu-id="cc000-137">指定要建立管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc000-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc000-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc000-138">-ResourceGroupName</span></span>
<span data-ttu-id="cc000-139">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc000-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cc000-140">此 Cmdlet 會為此參數指定的群組建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc000-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc000-141">-確認</span><span class="sxs-lookup"><span data-stu-id="cc000-141">-Confirm</span></span>
<span data-ttu-id="cc000-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc000-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc000-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc000-143">-WhatIf</span></span>
<span data-ttu-id="cc000-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc000-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc000-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc000-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc000-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc000-146">CommonParameters</span></span>
<span data-ttu-id="cc000-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc000-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc000-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cc000-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc000-149">輸入</span><span class="sxs-lookup"><span data-stu-id="cc000-149">INPUTS</span></span>

### <span data-ttu-id="cc000-150">System.String</span><span class="sxs-lookup"><span data-stu-id="cc000-150">System.String</span></span>

### <span data-ttu-id="cc000-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cc000-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="cc000-152">輸出</span><span class="sxs-lookup"><span data-stu-id="cc000-152">OUTPUTS</span></span>

### <span data-ttu-id="cc000-153">Microsoft.Azure.Commands.DataFactories.models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cc000-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="cc000-154">筆記</span><span class="sxs-lookup"><span data-stu-id="cc000-154">NOTES</span></span>
* <span data-ttu-id="cc000-155">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="cc000-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cc000-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc000-156">RELATED LINKS</span></span>

[<span data-ttu-id="cc000-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cc000-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="cc000-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cc000-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="cc000-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cc000-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="cc000-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="cc000-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="cc000-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cc000-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


