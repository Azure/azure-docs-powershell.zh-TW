---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449421"
---
# <span data-ttu-id="d2f71-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d2f71-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="d2f71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2f71-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f71-103">取得資料工廠中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f71-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="d2f71-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2f71-104">SYNTAX</span></span>

### <span data-ttu-id="d2f71-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d2f71-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2f71-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d2f71-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2f71-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f71-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2f71-108">說明</span><span class="sxs-lookup"><span data-stu-id="d2f71-108">DESCRIPTION</span></span>
<span data-ttu-id="d2f71-109">Get-AzDataFactoryV2Pipeline Cmdlet 會取得 Azure 資料工廠中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f71-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="d2f71-110">如果您指定管線的名稱，此 Cmdlet 會取得該管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f71-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="d2f71-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f71-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="d2f71-112">示例</span><span class="sxs-lookup"><span data-stu-id="d2f71-112">EXAMPLES</span></span>

### <span data-ttu-id="d2f71-113">範例1：取得所有管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d2f71-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="d2f71-114">這個命令會取得資料工廠（名為 WikiADF）中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f71-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="d2f71-115">您可以使用下列其中一個範例命令。</span><span class="sxs-lookup"><span data-stu-id="d2f71-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="d2f71-116">第二個是使用 DataFactory 物件做為參數。</span><span class="sxs-lookup"><span data-stu-id="d2f71-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="d2f71-117">範例2：取得特定管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d2f71-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="d2f71-118">這個命令會在名為 WikiADF 的資料工廠中，取得名為 DPWikisample 的管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f71-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d2f71-119">命令會使用管線運算子，將該資訊傳遞給 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2f71-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d2f71-120">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="d2f71-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d2f71-121">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="d2f71-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="d2f71-122">範例3：取得特定管線的屬性</span><span class="sxs-lookup"><span data-stu-id="d2f71-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="d2f71-123">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的活動屬性。</span><span class="sxs-lookup"><span data-stu-id="d2f71-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="d2f71-124">範例4：取得第一個活動的輸入資訊</span><span class="sxs-lookup"><span data-stu-id="d2f71-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="d2f71-125">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的活動屬性。</span><span class="sxs-lookup"><span data-stu-id="d2f71-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="d2f71-126">此命令會使用 Format-List Cmdlet 來顯示活動陣列第一個元素的 [輸入] 屬性。</span><span class="sxs-lookup"><span data-stu-id="d2f71-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="d2f71-127">參數</span><span class="sxs-lookup"><span data-stu-id="d2f71-127">PARAMETERS</span></span>

### <span data-ttu-id="d2f71-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d2f71-128">-DataFactory</span></span>
<span data-ttu-id="d2f71-129">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="d2f71-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="d2f71-130">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="d2f71-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2f71-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d2f71-131">-DataFactoryName</span></span>
<span data-ttu-id="d2f71-132">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f71-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d2f71-133">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="d2f71-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2f71-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f71-134">-DefaultProfile</span></span>
<span data-ttu-id="d2f71-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2f71-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f71-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2f71-136">-Name</span></span>
<span data-ttu-id="d2f71-137">指定要取得資訊的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f71-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="d2f71-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f71-138">-ResourceGroupName</span></span>
<span data-ttu-id="d2f71-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f71-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d2f71-140">這個 Cmdlet 會取得屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="d2f71-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2f71-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f71-141">-ResourceId</span></span>
<span data-ttu-id="d2f71-142">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2f71-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d2f71-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f71-143">CommonParameters</span></span>
<span data-ttu-id="d2f71-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2f71-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f71-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2f71-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f71-146">輸入</span><span class="sxs-lookup"><span data-stu-id="d2f71-146">INPUTS</span></span>

### <span data-ttu-id="d2f71-147">System.object</span><span class="sxs-lookup"><span data-stu-id="d2f71-147">System.String</span></span>

### <span data-ttu-id="d2f71-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d2f71-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d2f71-149">輸出</span><span class="sxs-lookup"><span data-stu-id="d2f71-149">OUTPUTS</span></span>

### <span data-ttu-id="d2f71-150">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d2f71-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="d2f71-151">筆記</span><span class="sxs-lookup"><span data-stu-id="d2f71-151">NOTES</span></span>
<span data-ttu-id="d2f71-152">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="d2f71-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d2f71-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2f71-153">RELATED LINKS</span></span>

[<span data-ttu-id="d2f71-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d2f71-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d2f71-155">移除-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d2f71-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d2f71-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d2f71-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
