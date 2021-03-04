---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: cd110ebf3b8467e1590ddf52a28d822eebe17092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907710"
---
# <span data-ttu-id="bde3f-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bde3f-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="bde3f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bde3f-102">SYNOPSIS</span></span>
<span data-ttu-id="bde3f-103">在 Data Factory 中收集管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bde3f-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="bde3f-104">語法</span><span class="sxs-lookup"><span data-stu-id="bde3f-104">SYNTAX</span></span>

### <span data-ttu-id="bde3f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="bde3f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bde3f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bde3f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bde3f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bde3f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bde3f-108">描述</span><span class="sxs-lookup"><span data-stu-id="bde3f-108">DESCRIPTION</span></span>
<span data-ttu-id="bde3f-109">Cmdlet Get-AzDataFactoryV2Pipeline Azure Data Factory 中的管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bde3f-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="bde3f-110">如果您指定管線的名稱，此 Cmdlet 會獲得該管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bde3f-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="bde3f-111">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="bde3f-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="bde3f-112">例子</span><span class="sxs-lookup"><span data-stu-id="bde3f-112">EXAMPLES</span></span>

### <span data-ttu-id="bde3f-113">範例 1：取得所有管線的資訊</span><span class="sxs-lookup"><span data-stu-id="bde3f-113">Example 1: Get information about all pipelines</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="bde3f-114">此命令會獲得名稱為 WikiADF 的資料工廠中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="bde3f-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="bde3f-115">您可以使用下列其中一個範例命令。</span><span class="sxs-lookup"><span data-stu-id="bde3f-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="bde3f-116">第二個則使用 DataFactory 物件做為參數。</span><span class="sxs-lookup"><span data-stu-id="bde3f-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="bde3f-117">範例 2：取得特定管線的資訊</span><span class="sxs-lookup"><span data-stu-id="bde3f-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="bde3f-118">此命令會從名為 WikiADF 的資料工廠中，獲得名為DPWikisample 的管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bde3f-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="bde3f-119">命令會使用管線運算子Format-List Cmdlet 將該資訊傳遞至該 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bde3f-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bde3f-120">Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="bde3f-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="bde3f-121">詳細資訊，輸入Get-Help格式清單。</span><span class="sxs-lookup"><span data-stu-id="bde3f-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="bde3f-122">範例 3：取得特定管線的屬性</span><span class="sxs-lookup"><span data-stu-id="bde3f-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="bde3f-123">此命令會針對名為 WikiADF 的資料工廠中名為DPWikisample的管線，獲得相關資訊，然後使用標準點標記法來查看與該管線相關聯的活動屬性。</span><span class="sxs-lookup"><span data-stu-id="bde3f-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="bde3f-124">範例 4：取得第一個活動輸入的資訊</span><span class="sxs-lookup"><span data-stu-id="bde3f-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="bde3f-125">此命令會針對名為 WikiADF 的資料工廠中名為DPWikisample的管線，獲得相關資訊，然後使用標準點標記法來查看與該管線相關聯的活動屬性。</span><span class="sxs-lookup"><span data-stu-id="bde3f-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="bde3f-126">命令會使用 Cmdlet 來顯示活動陣列中第一個元素的 Inputs 屬性Format-List。</span><span class="sxs-lookup"><span data-stu-id="bde3f-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="bde3f-127">參數</span><span class="sxs-lookup"><span data-stu-id="bde3f-127">PARAMETERS</span></span>

### <span data-ttu-id="bde3f-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bde3f-128">-DataFactory</span></span>
<span data-ttu-id="bde3f-129">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="bde3f-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="bde3f-130">此 Cmdlet 會獲得屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="bde3f-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bde3f-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bde3f-131">-DataFactoryName</span></span>
<span data-ttu-id="bde3f-132">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde3f-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bde3f-133">此 Cmdlet 會獲得屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="bde3f-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bde3f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde3f-134">-DefaultProfile</span></span>
<span data-ttu-id="bde3f-135">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bde3f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bde3f-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="bde3f-136">-Name</span></span>
<span data-ttu-id="bde3f-137">指定要取得相關資訊的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="bde3f-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde3f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde3f-138">-ResourceGroupName</span></span>
<span data-ttu-id="bde3f-139">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde3f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bde3f-140">此 Cmdlet 會獲得屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="bde3f-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bde3f-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bde3f-141">-ResourceId</span></span>
<span data-ttu-id="bde3f-142">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bde3f-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bde3f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde3f-143">CommonParameters</span></span>
<span data-ttu-id="bde3f-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bde3f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde3f-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bde3f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde3f-146">輸入</span><span class="sxs-lookup"><span data-stu-id="bde3f-146">INPUTS</span></span>

### <span data-ttu-id="bde3f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bde3f-147">System.String</span></span>

### <span data-ttu-id="bde3f-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bde3f-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bde3f-149">輸出</span><span class="sxs-lookup"><span data-stu-id="bde3f-149">OUTPUTS</span></span>

### <span data-ttu-id="bde3f-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="bde3f-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="bde3f-151">筆記</span><span class="sxs-lookup"><span data-stu-id="bde3f-151">NOTES</span></span>
<span data-ttu-id="bde3f-152">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="bde3f-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bde3f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="bde3f-153">RELATED LINKS</span></span>

[<span data-ttu-id="bde3f-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bde3f-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="bde3f-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bde3f-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="bde3f-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bde3f-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
