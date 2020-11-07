---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 50942dfc9b31b96a796b0a77df8b1ffc1a4cbd36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626111"
---
# <span data-ttu-id="680b4-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="680b4-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="680b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="680b4-102">SYNOPSIS</span></span>
<span data-ttu-id="680b4-103">取得 Azure 資料工廠中資料集的資料切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="680b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="680b4-104">SYNTAX</span></span>

### <span data-ttu-id="680b4-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="680b4-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="680b4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="680b4-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="680b4-107">說明</span><span class="sxs-lookup"><span data-stu-id="680b4-107">DESCRIPTION</span></span>
<span data-ttu-id="680b4-108">**AzureRmDataFactorySlice** Cmdlet 會取得 Azure 資料工廠中資料集的資料切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="680b4-109">指定 [開始時間] 和 [結束時間]，以定義要查看的資料切片範圍。</span><span class="sxs-lookup"><span data-stu-id="680b4-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="680b4-110">資料切片的狀態是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="680b4-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="680b4-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="680b4-111">PendingExecution.</span></span>
<span data-ttu-id="680b4-112">尚未開始進行資料處理。</span><span class="sxs-lookup"><span data-stu-id="680b4-112">Data processing has not started.</span></span> 
- <span data-ttu-id="680b4-113">正在.</span><span class="sxs-lookup"><span data-stu-id="680b4-113">InProgress.</span></span>
<span data-ttu-id="680b4-114">正在進行資料處理。</span><span class="sxs-lookup"><span data-stu-id="680b4-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="680b4-115">即可.</span><span class="sxs-lookup"><span data-stu-id="680b4-115">Ready.</span></span>
<span data-ttu-id="680b4-116">已完成資料處理。</span><span class="sxs-lookup"><span data-stu-id="680b4-116">Data processing is completed.</span></span>
<span data-ttu-id="680b4-117">資料切片已就緒，可供相依切片使用。</span><span class="sxs-lookup"><span data-stu-id="680b4-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="680b4-118">成功.</span><span class="sxs-lookup"><span data-stu-id="680b4-118">Failed.</span></span>
<span data-ttu-id="680b4-119">產生切片的執行失敗。</span><span class="sxs-lookup"><span data-stu-id="680b4-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="680b4-120">跳.</span><span class="sxs-lookup"><span data-stu-id="680b4-120">Skip.</span></span>
<span data-ttu-id="680b4-121">資料工廠會跳過切片的處理。</span><span class="sxs-lookup"><span data-stu-id="680b4-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="680b4-122">重試.</span><span class="sxs-lookup"><span data-stu-id="680b4-122">Retry.</span></span>
<span data-ttu-id="680b4-123">資料工廠會將產生扇面的執行重試。</span><span class="sxs-lookup"><span data-stu-id="680b4-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="680b4-124">已超時。資料處理已超時。</span><span class="sxs-lookup"><span data-stu-id="680b4-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="680b4-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="680b4-125">PendingValidation.</span></span>
<span data-ttu-id="680b4-126">資料切片在進行處理之前，正在等待驗證。</span><span class="sxs-lookup"><span data-stu-id="680b4-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="680b4-127">[重試驗證]。</span><span class="sxs-lookup"><span data-stu-id="680b4-127">Retry Validation.</span></span>
<span data-ttu-id="680b4-128">資料工廠會重試切片的驗證。</span><span class="sxs-lookup"><span data-stu-id="680b4-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="680b4-129">驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="680b4-129">Failed Validation.</span></span>
<span data-ttu-id="680b4-130">切片驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="680b4-130">Validation of the slice failed.</span></span>
<span data-ttu-id="680b4-131">針對每個扇面，您可以使用 Get-AzureRmDataFactoryRun Cmdlet 來查看產生切片的執行的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="680b4-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="680b4-132">示例</span><span class="sxs-lookup"><span data-stu-id="680b4-132">EXAMPLES</span></span>

### <span data-ttu-id="680b4-133">範例1：取得資料集的資料切片</span><span class="sxs-lookup"><span data-stu-id="680b4-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="680b4-134">這個命令會在名為 WikiADF 的資料工廠中，取得名為 WikiAggregatedData 的資料集的所有資料切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="680b4-135">命令會在 StartDateTime 參數指定的時間之後，取得所產生的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="680b4-136">下列範例程式碼會針對 JavaScript 物件符號 (JSON) 檔案中的每小時，設定這個資料集的可用性。</span><span class="sxs-lookup"><span data-stu-id="680b4-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="680b4-137">可用性： {period： "Hour"，periodMultiplier： 1} 部分結果已準備好，其他則是 PendingExecution。</span><span class="sxs-lookup"><span data-stu-id="680b4-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="680b4-138">已執行就緒的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-138">Ready slices have already run.</span></span>
<span data-ttu-id="680b4-139">擱置中的切片會在 Set-AzureRmDataFactoryPipelineActivePeriod Cmdlet 指定的間隔時間結束時，等待執行。</span><span class="sxs-lookup"><span data-stu-id="680b4-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="680b4-140">在這個範例中，管線和扇面的開始和結束期間都有一天的值 (24 小時) 。</span><span class="sxs-lookup"><span data-stu-id="680b4-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="680b4-141">參數</span><span class="sxs-lookup"><span data-stu-id="680b4-141">PARAMETERS</span></span>

### <span data-ttu-id="680b4-142">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="680b4-142">-DataFactory</span></span>
<span data-ttu-id="680b4-143">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="680b4-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="680b4-144">這個 Cmdlet 會取得屬於此參數指定之資料工廠的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="680b4-145">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="680b4-145">-DataFactoryName</span></span>
<span data-ttu-id="680b4-146">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="680b4-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="680b4-147">這個 Cmdlet 會取得屬於此參數指定之資料工廠的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="680b4-148">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="680b4-148">-DatasetName</span></span>
<span data-ttu-id="680b4-149">指定此 Cmdlet 取得其扇面的資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="680b4-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="680b4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="680b4-150">-DefaultProfile</span></span>
<span data-ttu-id="680b4-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="680b4-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="680b4-152">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="680b4-152">-EndDateTime</span></span>
<span data-ttu-id="680b4-153">將時段的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="680b4-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="680b4-154">這個 Cmdlet 會取得此參數指定時間之前所產生的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="680b4-155">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="680b4-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="680b4-156">*EndDateTime* 必須在 ISO8601 格式中指定，如下列範例所示： 2015-01-01Z 2015-01-01T00 .. 00： 00Z 2015-01-01T00：00： 00.000 z (UTC) 2015-01-01T00：00：00： 00 (太平洋標準時間) 預設的時區指示符是 UTC。</span><span class="sxs-lookup"><span data-stu-id="680b4-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="680b4-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="680b4-157">-ResourceGroupName</span></span>
<span data-ttu-id="680b4-158">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="680b4-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="680b4-159">這個 Cmdlet 會取得屬於此參數指定之群組的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="680b4-160">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="680b4-160">-StartDateTime</span></span>
<span data-ttu-id="680b4-161">指定時段的開頭作為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="680b4-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="680b4-162">這個 Cmdlet 會取得此參數指定時間之後所產生的切片。</span><span class="sxs-lookup"><span data-stu-id="680b4-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="680b4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680b4-163">CommonParameters</span></span>
<span data-ttu-id="680b4-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="680b4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680b4-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="680b4-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680b4-166">輸入</span><span class="sxs-lookup"><span data-stu-id="680b4-166">INPUTS</span></span>

### <span data-ttu-id="680b4-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="680b4-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="680b4-168">System.object</span><span class="sxs-lookup"><span data-stu-id="680b4-168">System.String</span></span>

## <span data-ttu-id="680b4-169">輸出</span><span class="sxs-lookup"><span data-stu-id="680b4-169">OUTPUTS</span></span>

### <span data-ttu-id="680b4-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="680b4-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="680b4-171">筆記</span><span class="sxs-lookup"><span data-stu-id="680b4-171">NOTES</span></span>
* <span data-ttu-id="680b4-172">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="680b4-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="680b4-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="680b4-173">RELATED LINKS</span></span>

[<span data-ttu-id="680b4-174">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="680b4-174">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="680b4-175">AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="680b4-175">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="680b4-176">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="680b4-176">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


