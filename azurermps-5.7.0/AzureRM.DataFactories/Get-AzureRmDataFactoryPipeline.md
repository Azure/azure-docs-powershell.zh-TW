---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 17a6be37e62693f3e6d6e7c9089f72771fc0a9f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444628"
---
# <span data-ttu-id="17ccf-101">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17ccf-101">Get-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="17ccf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="17ccf-103">取得有關 Azure 資料工廠中管道的資訊。</span><span class="sxs-lookup"><span data-stu-id="17ccf-103">Gets information about pipelines in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17ccf-104">句法</span><span class="sxs-lookup"><span data-stu-id="17ccf-104">SYNTAX</span></span>

### <span data-ttu-id="17ccf-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="17ccf-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17ccf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="17ccf-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ccf-107">說明</span><span class="sxs-lookup"><span data-stu-id="17ccf-107">DESCRIPTION</span></span>
<span data-ttu-id="17ccf-108">**AzureRmDataFactoryPipeline** Cmdlet 會取得 Azure 資料工廠中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="17ccf-108">The **Get-AzureRmDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="17ccf-109">如果您指定管線的名稱，此 Cmdlet 會取得該管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="17ccf-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="17ccf-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="17ccf-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="17ccf-111">示例</span><span class="sxs-lookup"><span data-stu-id="17ccf-111">EXAMPLES</span></span>

### <span data-ttu-id="17ccf-112">範例1：取得所有管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="17ccf-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="17ccf-113">這個命令會取得資料工廠（名為 WikiADF）中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="17ccf-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="17ccf-114">您可以在下列其中一個範例命令。</span><span class="sxs-lookup"><span data-stu-id="17ccf-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="17ccf-115">第二個是使用 **DataFactory** 物件做為參數。</span><span class="sxs-lookup"><span data-stu-id="17ccf-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="17ccf-116">範例2：取得特定管線的相關資訊</span><span class="sxs-lookup"><span data-stu-id="17ccf-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="17ccf-117">這個命令會在名為 WikiADF 的資料工廠中，取得名為 DPWikisample 的管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="17ccf-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="17ccf-118">命令會使用管線運算子，將該資訊傳遞給 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17ccf-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="17ccf-119">該 Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="17ccf-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="17ccf-120">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="17ccf-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="17ccf-121">範例3：取得特定管線的屬性</span><span class="sxs-lookup"><span data-stu-id="17ccf-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="17ccf-122">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線關聯的 **Properties** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17ccf-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="17ccf-123">範例4：取得特定管線的活動</span><span class="sxs-lookup"><span data-stu-id="17ccf-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
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

<span data-ttu-id="17ccf-124">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的 **活動** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17ccf-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="17ccf-125">範例5：取得特定管線的執行時間資訊</span><span class="sxs-lookup"><span data-stu-id="17ccf-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="17ccf-126">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的 **RuntimeInfo** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17ccf-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="17ccf-127">範例6：取得第一個活動的輸入資訊</span><span class="sxs-lookup"><span data-stu-id="17ccf-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="17ccf-128">這個命令會取得名為 WikiADF 之資料工廠中名為 DPWikisample 的管線資訊，然後使用標準點符號來查看與該管線相關聯的 **活動** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17ccf-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="17ccf-129">此命令會使用 [ **格式] 清單** ，顯示 **活動** 陣列第一個元素的 [ **輸入** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="17ccf-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="17ccf-130">參數</span><span class="sxs-lookup"><span data-stu-id="17ccf-130">PARAMETERS</span></span>

### <span data-ttu-id="17ccf-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="17ccf-131">-DataFactory</span></span>
<span data-ttu-id="17ccf-132">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="17ccf-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="17ccf-133">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="17ccf-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ccf-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="17ccf-134">-DataFactoryName</span></span>
<span data-ttu-id="17ccf-135">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="17ccf-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="17ccf-136">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="17ccf-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="17ccf-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ccf-137">-DefaultProfile</span></span>
<span data-ttu-id="17ccf-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="17ccf-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ccf-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="17ccf-139">-Name</span></span>
<span data-ttu-id="17ccf-140">指定要取得資訊的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="17ccf-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ccf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ccf-141">-ResourceGroupName</span></span>
<span data-ttu-id="17ccf-142">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17ccf-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="17ccf-143">這個 Cmdlet 會取得屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="17ccf-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="17ccf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ccf-144">CommonParameters</span></span>
<span data-ttu-id="17ccf-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17ccf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ccf-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17ccf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ccf-147">輸入</span><span class="sxs-lookup"><span data-stu-id="17ccf-147">INPUTS</span></span>

### <span data-ttu-id="17ccf-148">所有</span><span class="sxs-lookup"><span data-stu-id="17ccf-148">None</span></span>
<span data-ttu-id="17ccf-149">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="17ccf-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17ccf-150">輸出</span><span class="sxs-lookup"><span data-stu-id="17ccf-150">OUTPUTS</span></span>

### <span data-ttu-id="17ccf-151">[System.object]. 清單 ' 1 [PSPipeline，WindowsAzure. WindowsAzure = 0.8.2.0，Culture = 中立，PublicKeyToken = 31bf3856ad364e35]]. WindowsAzure. PSPipeline.）的。。</span><span class="sxs-lookup"><span data-stu-id="17ccf-151">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSPipeline, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="17ccf-152">筆記</span><span class="sxs-lookup"><span data-stu-id="17ccf-152">NOTES</span></span>
* <span data-ttu-id="17ccf-153">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="17ccf-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="17ccf-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="17ccf-154">RELATED LINKS</span></span>

[<span data-ttu-id="17ccf-155">新-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17ccf-155">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="17ccf-156">移除-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17ccf-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="17ccf-157">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17ccf-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="17ccf-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="17ccf-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="17ccf-159">暫停-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17ccf-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


