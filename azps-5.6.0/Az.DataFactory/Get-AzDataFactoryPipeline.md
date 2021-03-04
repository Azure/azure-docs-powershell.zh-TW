---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907774"
---
# <span data-ttu-id="1dc09-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1dc09-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="1dc09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dc09-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc09-103">在 Azure Data Factory 中收集管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc09-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="1dc09-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dc09-104">SYNTAX</span></span>

### <span data-ttu-id="1dc09-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="1dc09-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc09-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1dc09-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc09-107">描述</span><span class="sxs-lookup"><span data-stu-id="1dc09-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc09-108">**Get-AzDataFactoryPipeline Cmdlet** 會取得 Azure Data Factory 中管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc09-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="1dc09-109">如果您指定管線的名稱，此 Cmdlet 會獲得該管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc09-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="1dc09-110">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc09-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="1dc09-111">例子</span><span class="sxs-lookup"><span data-stu-id="1dc09-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc09-112">範例 1：取得所有管線的資訊</span><span class="sxs-lookup"><span data-stu-id="1dc09-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="1dc09-113">此命令會獲得名稱為 WikiADF 的資料工廠中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc09-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="1dc09-114">您可以執行下列其中一個範例命令。</span><span class="sxs-lookup"><span data-stu-id="1dc09-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="1dc09-115">第二個則使用 **DataFactory** 物件做為參數。</span><span class="sxs-lookup"><span data-stu-id="1dc09-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="1dc09-116">範例 2：取得特定管線的資訊</span><span class="sxs-lookup"><span data-stu-id="1dc09-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="1dc09-117">此命令會從名為 WikiADF 的資料工廠中，獲得名為DPWikisample 的管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc09-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="1dc09-118">命令會使用管線運算子Format-List Cmdlet 將該資訊傳遞至該 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dc09-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1dc09-119">該 Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="1dc09-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="1dc09-120">如需要詳細資訊，請鍵入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="1dc09-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="1dc09-121">範例 3：取得特定管線的屬性</span><span class="sxs-lookup"><span data-stu-id="1dc09-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="1dc09-122">此命令會針對名為 WikiADF 的資料工廠中名為DPWikisample 的管線，獲得相關資訊，然後使用標準點標記法來查看與該管線相關聯的 Properties 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc09-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="1dc09-123">範例 4：取得特定管線的活動</span><span class="sxs-lookup"><span data-stu-id="1dc09-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="1dc09-124">此命令會針對名為 WikiADF 的資料工廠中名為DPWikisample的管線，獲得相關資訊，然後使用標準點標記法來查看與該管線相關聯的 **活動** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc09-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="1dc09-125">範例 5：取得特定管線的執行時間資訊</span><span class="sxs-lookup"><span data-stu-id="1dc09-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="1dc09-126">此命令會針對名為 WikiADF 的資料工廠中名為DPWikisample 的管線，獲得相關資訊，然後使用標準點標記法來查看與該管線相關聯的 **RuntimeInfo** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc09-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="1dc09-127">範例 6：取得第一個活動輸入的資訊</span><span class="sxs-lookup"><span data-stu-id="1dc09-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="1dc09-128">此命令會針對名為 WikiADF 的資料工廠中名為DPWikisample的管線，獲得相關資訊，然後使用標準點標記法來查看與該管線相關聯的 **活動** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc09-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="1dc09-129">命令會使用 **Format-List** 顯示 **Activities** 陣列中第一個元素的 **Inputs** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc09-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="1dc09-130">參數</span><span class="sxs-lookup"><span data-stu-id="1dc09-130">PARAMETERS</span></span>

### <span data-ttu-id="1dc09-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc09-131">-DataFactory</span></span>
<span data-ttu-id="1dc09-132">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="1dc09-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1dc09-133">此 Cmdlet 會獲得屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="1dc09-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dc09-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1dc09-134">-DataFactoryName</span></span>
<span data-ttu-id="1dc09-135">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc09-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1dc09-136">此 Cmdlet 會獲得屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="1dc09-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dc09-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc09-137">-DefaultProfile</span></span>
<span data-ttu-id="1dc09-138">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1dc09-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dc09-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dc09-139">-Name</span></span>
<span data-ttu-id="1dc09-140">指定要取得相關資訊的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc09-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="1dc09-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc09-141">-ResourceGroupName</span></span>
<span data-ttu-id="1dc09-142">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc09-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1dc09-143">此 Cmdlet 會獲得屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="1dc09-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dc09-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc09-144">CommonParameters</span></span>
<span data-ttu-id="1dc09-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dc09-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc09-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1dc09-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc09-147">輸入</span><span class="sxs-lookup"><span data-stu-id="1dc09-147">INPUTS</span></span>

### <span data-ttu-id="1dc09-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1dc09-148">System.String</span></span>

### <span data-ttu-id="1dc09-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc09-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1dc09-150">輸出</span><span class="sxs-lookup"><span data-stu-id="1dc09-150">OUTPUTS</span></span>

### <span data-ttu-id="1dc09-151">Microsoft.Azure.Commands.DataFactories.models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1dc09-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="1dc09-152">筆記</span><span class="sxs-lookup"><span data-stu-id="1dc09-152">NOTES</span></span>
* <span data-ttu-id="1dc09-153">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="1dc09-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1dc09-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dc09-154">RELATED LINKS</span></span>

[<span data-ttu-id="1dc09-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1dc09-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="1dc09-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1dc09-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="1dc09-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1dc09-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="1dc09-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1dc09-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1dc09-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1dc09-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


