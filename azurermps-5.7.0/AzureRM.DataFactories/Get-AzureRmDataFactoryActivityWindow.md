---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 33deeafce23267d1b2dbc594251bc58de1914280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444627"
---
# <span data-ttu-id="71e95-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="71e95-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="71e95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71e95-102">SYNOPSIS</span></span>
<span data-ttu-id="71e95-103">取得與資料工廠關聯之使用中視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71e95-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e95-104">句法</span><span class="sxs-lookup"><span data-stu-id="71e95-104">SYNTAX</span></span>

### <span data-ttu-id="71e95-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="71e95-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="71e95-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71e95-107">說明</span><span class="sxs-lookup"><span data-stu-id="71e95-107">DESCRIPTION</span></span>
<span data-ttu-id="71e95-108">**AzureRmDataFactoryActivityWindow** Cmdlet 會取得與資料工廠關聯之使用中視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71e95-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="71e95-109">示例</span><span class="sxs-lookup"><span data-stu-id="71e95-109">EXAMPLES</span></span>

### <span data-ttu-id="71e95-110">範例1：取得與資料工廠相關聯的使用中視窗</span><span class="sxs-lookup"><span data-stu-id="71e95-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="71e95-111">這個命令會取得與名為 WikiADF 的資料工廠相關聯之所有使用中視窗的資訊。</span><span class="sxs-lookup"><span data-stu-id="71e95-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="71e95-112">參數</span><span class="sxs-lookup"><span data-stu-id="71e95-112">PARAMETERS</span></span>

### <span data-ttu-id="71e95-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="71e95-113">-ActivityName</span></span>
<span data-ttu-id="71e95-114">指定活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e95-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="71e95-115">這個 Cmdlet 會取得此參數指定之活動的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="71e95-116">-DataFactory</span></span>
<span data-ttu-id="71e95-117">指定由 Cmdlet 傳回的 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="71e95-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="71e95-118">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="71e95-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="71e95-119">-DataFactoryName</span></span>
<span data-ttu-id="71e95-120">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e95-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="71e95-121">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="71e95-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="71e95-122">-DatasetName</span></span>
<span data-ttu-id="71e95-123">指定資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e95-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="71e95-124">這個 Cmdlet 會取得屬於此參數所指定之資料集的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e95-125">-DefaultProfile</span></span>
<span data-ttu-id="71e95-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="71e95-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e95-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="71e95-127">-Filter</span></span>
<span data-ttu-id="71e95-128">指定使用 Azure 搜尋篩選文法來表示的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="71e95-129">如需文法的相關資訊，請參閱 MSDN 中的 Azure Search (OData 運算式語法 https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="71e95-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="71e95-130">使用中視窗清單會依據此參數指定的搜尋字串篩選。</span><span class="sxs-lookup"><span data-stu-id="71e95-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="71e95-131">-OrderBy</span></span>
<span data-ttu-id="71e95-132">指定要依其中一個使用中視窗清單參數來排序回應。</span><span class="sxs-lookup"><span data-stu-id="71e95-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="71e95-133">這是以逗號分隔的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="71e95-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="71e95-134">例如： WindowStart，百分比。</span><span class="sxs-lookup"><span data-stu-id="71e95-134">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="71e95-135">根據預設，順序是 (ASC) 的昇冪順序。</span><span class="sxs-lookup"><span data-stu-id="71e95-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="71e95-136">如果您想要以遞減順序排序清單，請指定 DESC。</span><span class="sxs-lookup"><span data-stu-id="71e95-136">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="71e95-137">-PipelineName</span></span>
<span data-ttu-id="71e95-138">指定管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e95-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="71e95-139">這個 Cmdlet 會取得屬於此參數所指定管線的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e95-140">-ResourceGroupName</span></span>
<span data-ttu-id="71e95-141">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e95-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="71e95-142">這個 Cmdlet 會取得屬於此參數指定之資源群組的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="71e95-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="71e95-143">-RunEnd</span></span>
<span data-ttu-id="71e95-144">指定使用中視窗執行的結束時間。</span><span class="sxs-lookup"><span data-stu-id="71e95-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="71e95-145">這個 Cmdlet 會取得執行時間落在 *RunStart* 和 *RunEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="71e95-146">-RunStart</span></span>
<span data-ttu-id="71e95-147">指定使用中視窗執行的開始時間。</span><span class="sxs-lookup"><span data-stu-id="71e95-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="71e95-148">這個 Cmdlet 會取得執行時間落在 *RunStart* 和 *RunEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-149">-上方</span><span class="sxs-lookup"><span data-stu-id="71e95-149">-Top</span></span>
<span data-ttu-id="71e95-150">指定此 Cmdlet 傳回的使用中視窗數目上限。</span><span class="sxs-lookup"><span data-stu-id="71e95-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="71e95-151">-WindowEnd</span></span>
<span data-ttu-id="71e95-152">指定使用中視窗的結束時間。</span><span class="sxs-lookup"><span data-stu-id="71e95-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="71e95-153">這個 Cmdlet 會取得時間落在 *WindowStart* 和 *WindowEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="71e95-154">-WindowStart</span></span>
<span data-ttu-id="71e95-155">指定 [活動] 視窗的開始時間。</span><span class="sxs-lookup"><span data-stu-id="71e95-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="71e95-156">這個 Cmdlet 會取得時間落在 *WindowStart* 和 *WindowEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="71e95-157">-WindowState</span></span>
<span data-ttu-id="71e95-158">指定使用中視窗的狀態。</span><span class="sxs-lookup"><span data-stu-id="71e95-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="71e95-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="71e95-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71e95-160">所有</span><span class="sxs-lookup"><span data-stu-id="71e95-160">None</span></span>
- <span data-ttu-id="71e95-161">等待</span><span class="sxs-lookup"><span data-stu-id="71e95-161">Waiting</span></span>
- <span data-ttu-id="71e95-162">正在</span><span class="sxs-lookup"><span data-stu-id="71e95-162">InProgress</span></span>
- <span data-ttu-id="71e95-163">即可</span><span class="sxs-lookup"><span data-stu-id="71e95-163">Ready</span></span>
- <span data-ttu-id="71e95-164">成功</span><span class="sxs-lookup"><span data-stu-id="71e95-164">Failed</span></span>
- <span data-ttu-id="71e95-165">略過</span><span class="sxs-lookup"><span data-stu-id="71e95-165">Skipped</span></span>

<span data-ttu-id="71e95-166">這個 Cmdlet 會取得此參數指定狀態的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-166">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-167">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="71e95-167">-WindowSubstate</span></span>
<span data-ttu-id="71e95-168">指定使用中視窗的子時間。</span><span class="sxs-lookup"><span data-stu-id="71e95-168">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="71e95-169">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="71e95-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71e95-170">取消</span><span class="sxs-lookup"><span data-stu-id="71e95-170">Canceled</span></span>
- <span data-ttu-id="71e95-171">timedOut</span><span class="sxs-lookup"><span data-stu-id="71e95-171">timedOut</span></span>
- <span data-ttu-id="71e95-172">確認</span><span class="sxs-lookup"><span data-stu-id="71e95-172">Validating</span></span>

<span data-ttu-id="71e95-173">這個 Cmdlet 會取得此參數指定之子類型中的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="71e95-173">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e95-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e95-174">CommonParameters</span></span>
<span data-ttu-id="71e95-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71e95-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e95-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71e95-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e95-177">輸入</span><span class="sxs-lookup"><span data-stu-id="71e95-177">INPUTS</span></span>

### <span data-ttu-id="71e95-178">所有</span><span class="sxs-lookup"><span data-stu-id="71e95-178">None</span></span>
<span data-ttu-id="71e95-179">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="71e95-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71e95-180">輸出</span><span class="sxs-lookup"><span data-stu-id="71e95-180">OUTPUTS</span></span>

### <span data-ttu-id="71e95-181">[System.object]。清單 ' 1 [PSActivyWindow，WindowsAzure. WindowsAzure = 0.8.2.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]」）））。</span><span class="sxs-lookup"><span data-stu-id="71e95-181">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="71e95-182">筆記</span><span class="sxs-lookup"><span data-stu-id="71e95-182">NOTES</span></span>

## <span data-ttu-id="71e95-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="71e95-183">RELATED LINKS</span></span>

[<span data-ttu-id="71e95-184">Azure 資料工廠 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71e95-184">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


