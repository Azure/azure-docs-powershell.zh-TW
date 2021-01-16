---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280950"
---
# <span data-ttu-id="b95ee-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b95ee-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="b95ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b95ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b95ee-103">取得有關 Azure 資料工廠中管道的資訊。</span><span class="sxs-lookup"><span data-stu-id="b95ee-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="b95ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="b95ee-104">SYNTAX</span></span>

### <span data-ttu-id="b95ee-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b95ee-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b95ee-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b95ee-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b95ee-107">說明</span><span class="sxs-lookup"><span data-stu-id="b95ee-107">DESCRIPTION</span></span>
<span data-ttu-id="b95ee-108">**AzDataFactoryPipeline** Cmdlet 會取得 Azure 資料工廠中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b95ee-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="b95ee-109">如果您指定管線的名稱，此 Cmdlet 會取得該管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b95ee-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="b95ee-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b95ee-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="b95ee-111">示例</span><span class="sxs-lookup"><span data-stu-id="b95ee-111">EXAMPLES</span></span>

### <span data-ttu-id="b95ee-112">範例1：取得所有管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b95ee-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="b95ee-113">這個命令會取得資料工廠（名為 WikiADF）中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b95ee-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="b95ee-114">您可以在下列其中一個範例命令。</span><span class="sxs-lookup"><span data-stu-id="b95ee-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="b95ee-115">第二個是使用 **DataFactory** 物件做為參數。</span><span class="sxs-lookup"><span data-stu-id="b95ee-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="b95ee-116">範例2：取得特定管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b95ee-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="b95ee-117">這個命令會在名為 WikiADF 的資料工廠中，取得名為 DPWikisample 的管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b95ee-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="b95ee-118">命令會使用管線運算子，將該資訊傳遞給 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b95ee-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b95ee-119">該 Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="b95ee-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="b95ee-120">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="b95ee-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="b95ee-121">範例3：取得特定管線的屬性</span><span class="sxs-lookup"><span data-stu-id="b95ee-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="b95ee-122">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線關聯的 **Properties** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b95ee-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="b95ee-123">範例4：取得特定管線的活動</span><span class="sxs-lookup"><span data-stu-id="b95ee-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="b95ee-124">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的 **活動** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b95ee-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="b95ee-125">範例5：取得特定管線的執行時間資訊</span><span class="sxs-lookup"><span data-stu-id="b95ee-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="b95ee-126">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的 **RuntimeInfo** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b95ee-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="b95ee-127">範例6：取得第一個活動的輸入資訊</span><span class="sxs-lookup"><span data-stu-id="b95ee-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="b95ee-128">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的 **活動** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b95ee-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="b95ee-129">此命令會使用 [**格式] 清單**，顯示 **活動** 陣列第一個元素的 [**輸入**] 屬性。</span><span class="sxs-lookup"><span data-stu-id="b95ee-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="b95ee-130">參數</span><span class="sxs-lookup"><span data-stu-id="b95ee-130">PARAMETERS</span></span>

### <span data-ttu-id="b95ee-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b95ee-131">-DataFactory</span></span>
<span data-ttu-id="b95ee-132">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="b95ee-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b95ee-133">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="b95ee-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b95ee-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b95ee-134">-DataFactoryName</span></span>
<span data-ttu-id="b95ee-135">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b95ee-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b95ee-136">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="b95ee-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b95ee-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95ee-137">-DefaultProfile</span></span>
<span data-ttu-id="b95ee-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b95ee-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b95ee-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="b95ee-139">-Name</span></span>
<span data-ttu-id="b95ee-140">指定要取得資訊的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="b95ee-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="b95ee-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95ee-141">-ResourceGroupName</span></span>
<span data-ttu-id="b95ee-142">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b95ee-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b95ee-143">這個 Cmdlet 會取得屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="b95ee-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b95ee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95ee-144">CommonParameters</span></span>
<span data-ttu-id="b95ee-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b95ee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95ee-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b95ee-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95ee-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b95ee-147">INPUTS</span></span>

### <span data-ttu-id="b95ee-148">System.object</span><span class="sxs-lookup"><span data-stu-id="b95ee-148">System.String</span></span>

### <span data-ttu-id="b95ee-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b95ee-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="b95ee-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b95ee-150">OUTPUTS</span></span>

### <span data-ttu-id="b95ee-151">PSPipeline 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="b95ee-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="b95ee-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b95ee-152">NOTES</span></span>
* <span data-ttu-id="b95ee-153">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b95ee-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b95ee-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b95ee-154">RELATED LINKS</span></span>

[<span data-ttu-id="b95ee-155">新-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b95ee-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="b95ee-156">移除-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b95ee-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="b95ee-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b95ee-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="b95ee-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="b95ee-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="b95ee-159">暫停-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b95ee-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


