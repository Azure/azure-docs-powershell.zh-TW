---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456748"
---
# <span data-ttu-id="9b2cd-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9b2cd-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="9b2cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2cd-103">取得資料工廠中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b2cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b2cd-104">SYNTAX</span></span>

### <span data-ttu-id="9b2cd-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="9b2cd-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="9b2cd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9b2cd-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="9b2cd-107">說明</span><span class="sxs-lookup"><span data-stu-id="9b2cd-107">DESCRIPTION</span></span>
<span data-ttu-id="9b2cd-108">Get-AzureRmDataFactoryV2Pipeline Cmdlet 會取得 Azure 資料工廠中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="9b2cd-109">如果您指定管線的名稱，此 Cmdlet 會取得該管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="9b2cd-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="9b2cd-111">示例</span><span class="sxs-lookup"><span data-stu-id="9b2cd-111">EXAMPLES</span></span>

### <span data-ttu-id="9b2cd-112">範例1：取得所有管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="9b2cd-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="9b2cd-113">這個命令會取得資料工廠（名為 WikiADF）中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="9b2cd-114">您可以使用下列其中一個範例命令。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="9b2cd-115">第二個是使用 DataFactory 物件做為參數。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="9b2cd-116">範例2：取得特定管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="9b2cd-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="9b2cd-117">這個命令會在名為 WikiADF 的資料工廠中，取得名為 DPWikisample 的管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="9b2cd-118">命令會使用管線運算子，將該資訊傳遞給 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9b2cd-119">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="9b2cd-120">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="9b2cd-121">範例3：取得特定管線的屬性</span><span class="sxs-lookup"><span data-stu-id="9b2cd-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

<span data-ttu-id="9b2cd-122">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的活動屬性。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="9b2cd-123">範例6：取得第一個活動的輸入資訊</span><span class="sxs-lookup"><span data-stu-id="9b2cd-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

<span data-ttu-id="9b2cd-124">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的活動屬性。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="9b2cd-125">此命令會使用 Format-List Cmdlet 來顯示活動陣列第一個元素的 [輸入] 屬性。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="9b2cd-126">參數</span><span class="sxs-lookup"><span data-stu-id="9b2cd-126">PARAMETERS</span></span>

### <span data-ttu-id="9b2cd-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b2cd-127">-DataFactory</span></span>
<span data-ttu-id="9b2cd-128">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="9b2cd-129">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2cd-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9b2cd-130">-DataFactoryName</span></span>
<span data-ttu-id="9b2cd-131">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9b2cd-132">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b2cd-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b2cd-133">-Name</span></span>
<span data-ttu-id="9b2cd-134">指定要取得資訊的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2cd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2cd-135">-ResourceGroupName</span></span>
<span data-ttu-id="9b2cd-136">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9b2cd-137">這個 Cmdlet 會取得屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="9b2cd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9b2cd-138">INPUTS</span></span>

### <span data-ttu-id="9b2cd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9b2cd-139">System.String</span></span>
<span data-ttu-id="9b2cd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b2cd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="9b2cd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9b2cd-141">OUTPUTS</span></span>

### <span data-ttu-id="9b2cd-142">[System.object]。清單 ' 1 [DataFactoryV2. PSPipeline，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="9b2cd-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9b2cd-143">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="9b2cd-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="9b2cd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9b2cd-144">NOTES</span></span>
<span data-ttu-id="9b2cd-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="9b2cd-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9b2cd-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b2cd-146">RELATED LINKS</span></span>
[<span data-ttu-id="9b2cd-147">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9b2cd-147">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9b2cd-148">移除-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9b2cd-148">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9b2cd-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9b2cd-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
