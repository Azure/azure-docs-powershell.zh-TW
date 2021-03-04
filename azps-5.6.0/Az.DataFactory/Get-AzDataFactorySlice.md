---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907750"
---
# <span data-ttu-id="1b751-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="1b751-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="1b751-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b751-102">SYNOPSIS</span></span>
<span data-ttu-id="1b751-103">在 Azure Data Factory 中為資料集獲取資料區。</span><span class="sxs-lookup"><span data-stu-id="1b751-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="1b751-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b751-104">SYNTAX</span></span>

### <span data-ttu-id="1b751-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="1b751-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b751-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b751-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b751-107">描述</span><span class="sxs-lookup"><span data-stu-id="1b751-107">DESCRIPTION</span></span>
<span data-ttu-id="1b751-108">**Get-AzDataFactorySlice** Cmdlet 會取得 Azure Data Factory 中資料集的資料區。</span><span class="sxs-lookup"><span data-stu-id="1b751-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="1b751-109">指定開始時間和結束時間，以定義要查看的資料區範圍。</span><span class="sxs-lookup"><span data-stu-id="1b751-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="1b751-110">資料區的狀態為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1b751-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="1b751-111">PendingExecution。</span><span class="sxs-lookup"><span data-stu-id="1b751-111">PendingExecution.</span></span>
<span data-ttu-id="1b751-112">尚未開始進行資料管理。</span><span class="sxs-lookup"><span data-stu-id="1b751-112">Data processing has not started.</span></span> 
- <span data-ttu-id="1b751-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="1b751-113">InProgress.</span></span>
<span data-ttu-id="1b751-114">正在處理資料。</span><span class="sxs-lookup"><span data-stu-id="1b751-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="1b751-115">準備。</span><span class="sxs-lookup"><span data-stu-id="1b751-115">Ready.</span></span>
<span data-ttu-id="1b751-116">資料處理已完成。</span><span class="sxs-lookup"><span data-stu-id="1b751-116">Data processing is completed.</span></span>
<span data-ttu-id="1b751-117">資料區已準備好供從屬區塊使用。</span><span class="sxs-lookup"><span data-stu-id="1b751-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="1b751-118">失敗。</span><span class="sxs-lookup"><span data-stu-id="1b751-118">Failed.</span></span>
<span data-ttu-id="1b751-119">產生該區塊的執行失敗。</span><span class="sxs-lookup"><span data-stu-id="1b751-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="1b751-120">跳。</span><span class="sxs-lookup"><span data-stu-id="1b751-120">Skip.</span></span>
<span data-ttu-id="1b751-121">Data Factory 會略過處理該區塊。</span><span class="sxs-lookup"><span data-stu-id="1b751-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="1b751-122">重試。</span><span class="sxs-lookup"><span data-stu-id="1b751-122">Retry.</span></span>
<span data-ttu-id="1b751-123">Data Factory 會重試產生該區塊的執行。</span><span class="sxs-lookup"><span data-stu-id="1b751-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="1b751-124">已達時日。資料處理已過時。</span><span class="sxs-lookup"><span data-stu-id="1b751-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="1b751-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="1b751-125">PendingValidation.</span></span>
<span data-ttu-id="1b751-126">資料交叉分析區正在等待驗證，然後再進行處理。</span><span class="sxs-lookup"><span data-stu-id="1b751-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="1b751-127">重試驗證。</span><span class="sxs-lookup"><span data-stu-id="1b751-127">Retry Validation.</span></span>
<span data-ttu-id="1b751-128">Data Factory 會重新驗證交叉分析區。</span><span class="sxs-lookup"><span data-stu-id="1b751-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="1b751-129">驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="1b751-129">Failed Validation.</span></span>
<span data-ttu-id="1b751-130">交叉區驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="1b751-130">Validation of the slice failed.</span></span>
<span data-ttu-id="1b751-131">針對每個區塊，您可以使用 Cmdlet 查看產生該區Get-AzDataFactoryRun詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1b751-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="1b751-132">例子</span><span class="sxs-lookup"><span data-stu-id="1b751-132">EXAMPLES</span></span>

### <span data-ttu-id="1b751-133">範例 1：取得資料集的資料區</span><span class="sxs-lookup"><span data-stu-id="1b751-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="1b751-134">此命令會針對名為 WikiADF 的資料工廠中名為 WikiAggregatedData 的資料集，獲得所有資料區。</span><span class="sxs-lookup"><span data-stu-id="1b751-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="1b751-135">該命令在 StartDateTime 參數指定的時間之後，就會產生區塊。</span><span class="sxs-lookup"><span data-stu-id="1b751-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="1b751-136">下列範例程式碼會每小時在 JSON 檔案的 JavaScript 物件標記法 (此) 可用性。</span><span class="sxs-lookup"><span data-stu-id="1b751-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="1b751-137">可用性：{ period： "Hour"， periodMultiplier： 1 } 部分結果已就緒，其他為 PendingExecution。</span><span class="sxs-lookup"><span data-stu-id="1b751-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="1b751-138">Ready slices have have run.</span><span class="sxs-lookup"><span data-stu-id="1b751-138">Ready slices have already run.</span></span>
<span data-ttu-id="1b751-139">擱置的區隔區會以每個小時結尾的間隔等待執行，Set-AzDataFactoryPipelineActivePeriod Cmdlet 指定的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="1b751-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="1b751-140">在此範例中，管線和區段的開始與結束期間都有 24 小時 (24 小時) 。</span><span class="sxs-lookup"><span data-stu-id="1b751-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="1b751-141">範例 2</span><span class="sxs-lookup"><span data-stu-id="1b751-141">Example 2</span></span>

<span data-ttu-id="1b751-142">在 Azure Data Factory 中為資料集獲取資料區。</span><span class="sxs-lookup"><span data-stu-id="1b751-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="1b751-143"> (自動) </span><span class="sxs-lookup"><span data-stu-id="1b751-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="1b751-144">參數</span><span class="sxs-lookup"><span data-stu-id="1b751-144">PARAMETERS</span></span>

### <span data-ttu-id="1b751-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b751-145">-DataFactory</span></span>
<span data-ttu-id="1b751-146">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="1b751-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1b751-147">此 Cmdlet 會獲得屬於此參數指定之資料工廠的區塊。</span><span class="sxs-lookup"><span data-stu-id="1b751-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b751-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1b751-148">-DataFactoryName</span></span>
<span data-ttu-id="1b751-149">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b751-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1b751-150">此 Cmdlet 會獲得屬於此參數指定之資料工廠的區塊。</span><span class="sxs-lookup"><span data-stu-id="1b751-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b751-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="1b751-151">-DatasetName</span></span>
<span data-ttu-id="1b751-152">指定此 Cmdlet 會獲得資料區之資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b751-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b751-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b751-153">-DefaultProfile</span></span>
<span data-ttu-id="1b751-154">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1b751-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b751-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="1b751-155">-EndDateTime</span></span>
<span data-ttu-id="1b751-156">將時間週期的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="1b751-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="1b751-157">此 Cmdlet 會在此參數指定之時間之前產生區塊。</span><span class="sxs-lookup"><span data-stu-id="1b751-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="1b751-158">有關 **DateTime** 物件的資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="1b751-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1b751-159">*EndDateTime* 必須以 ISO8601 格式指定，如下列範例所示：2015-01-01Z 2015-01T00：00：00Z 2015-01-01T00 ：00：00.000Z (UTC) 2015-01-01T00：00：00：00-08：00 (太平洋標準時間) 預設時區設計工具為 UTC。</span><span class="sxs-lookup"><span data-stu-id="1b751-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b751-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b751-160">-ResourceGroupName</span></span>
<span data-ttu-id="1b751-161">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b751-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b751-162">此 Cmdlet 會獲得屬於此參數指定之群組的區塊。</span><span class="sxs-lookup"><span data-stu-id="1b751-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b751-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="1b751-163">-StartDateTime</span></span>
<span data-ttu-id="1b751-164">將時間週期的開始指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="1b751-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="1b751-165">此 Cmdlet 會在此參數指定的時間之後產生切區。</span><span class="sxs-lookup"><span data-stu-id="1b751-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b751-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b751-166">CommonParameters</span></span>
<span data-ttu-id="1b751-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b751-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b751-168">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1b751-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b751-169">輸入</span><span class="sxs-lookup"><span data-stu-id="1b751-169">INPUTS</span></span>

### <span data-ttu-id="1b751-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b751-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1b751-171">System.String</span><span class="sxs-lookup"><span data-stu-id="1b751-171">System.String</span></span>

## <span data-ttu-id="1b751-172">輸出</span><span class="sxs-lookup"><span data-stu-id="1b751-172">OUTPUTS</span></span>

### <span data-ttu-id="1b751-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="1b751-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="1b751-174">筆記</span><span class="sxs-lookup"><span data-stu-id="1b751-174">NOTES</span></span>
* <span data-ttu-id="1b751-175">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="1b751-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b751-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b751-176">RELATED LINKS</span></span>

[<span data-ttu-id="1b751-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="1b751-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="1b751-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="1b751-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="1b751-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1b751-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


