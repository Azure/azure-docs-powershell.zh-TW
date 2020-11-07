---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623676"
---
# <span data-ttu-id="d8556-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="d8556-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="d8556-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8556-102">SYNOPSIS</span></span>
<span data-ttu-id="d8556-103">取得與資料工廠關聯之使用中視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d8556-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8556-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8556-104">SYNTAX</span></span>

### <span data-ttu-id="d8556-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d8556-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8556-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8556-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8556-107">說明</span><span class="sxs-lookup"><span data-stu-id="d8556-107">DESCRIPTION</span></span>
<span data-ttu-id="d8556-108">**AzureRmDataFactoryActivityWindow** Cmdlet 會取得與資料工廠關聯之使用中視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d8556-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="d8556-109">示例</span><span class="sxs-lookup"><span data-stu-id="d8556-109">EXAMPLES</span></span>

### <span data-ttu-id="d8556-110">範例1：取得與資料工廠相關聯的使用中視窗</span><span class="sxs-lookup"><span data-stu-id="d8556-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="d8556-111">這個命令會取得與名為 WikiADF 的資料工廠相關聯之所有使用中視窗的資訊。</span><span class="sxs-lookup"><span data-stu-id="d8556-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="d8556-112">參數</span><span class="sxs-lookup"><span data-stu-id="d8556-112">PARAMETERS</span></span>

### <span data-ttu-id="d8556-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="d8556-113">-ActivityName</span></span>
<span data-ttu-id="d8556-114">指定活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8556-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="d8556-115">這個 Cmdlet 會取得此參數指定之活動的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8556-116">-DataFactory</span></span>
<span data-ttu-id="d8556-117">指定由 Cmdlet 傳回的 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="d8556-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="d8556-118">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8556-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8556-119">-DataFactoryName</span></span>
<span data-ttu-id="d8556-120">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8556-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="d8556-121">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8556-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d8556-122">-DatasetName</span></span>
<span data-ttu-id="d8556-123">指定資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8556-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="d8556-124">這個 Cmdlet 會取得屬於此參數所指定之資料集的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="d8556-125">-Filter</span></span>
<span data-ttu-id="d8556-126">指定使用 Azure 搜尋篩選文法來表示的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="d8556-127">如需文法的相關資訊，請參閱 MSDN 中的 Azure Search (OData 運算式語法 https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d8556-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="d8556-128">使用中視窗清單會依據此參數指定的搜尋字串篩選。</span><span class="sxs-lookup"><span data-stu-id="d8556-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d8556-129">-OrderBy</span></span>
<span data-ttu-id="d8556-130">指定要依其中一個使用中視窗清單參數來排序回應。</span><span class="sxs-lookup"><span data-stu-id="d8556-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="d8556-131">這是以逗號分隔的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="d8556-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="d8556-132">例如： WindowStart，百分比。</span><span class="sxs-lookup"><span data-stu-id="d8556-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="d8556-133">根據預設，順序是 (ASC) 的昇冪順序。</span><span class="sxs-lookup"><span data-stu-id="d8556-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="d8556-134">如果您想要以遞減順序排序清單，請指定 DESC。</span><span class="sxs-lookup"><span data-stu-id="d8556-134">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d8556-135">-PipelineName</span></span>
<span data-ttu-id="d8556-136">指定管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8556-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="d8556-137">這個 Cmdlet 會取得屬於此參數所指定管線的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8556-138">-ResourceGroupName</span></span>
<span data-ttu-id="d8556-139">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8556-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="d8556-140">這個 Cmdlet 會取得屬於此參數指定之資源群組的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8556-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="d8556-141">-RunEnd</span></span>
<span data-ttu-id="d8556-142">指定使用中視窗執行的結束時間。</span><span class="sxs-lookup"><span data-stu-id="d8556-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="d8556-143">這個 Cmdlet 會取得執行時間落在 *RunStart* 和 *RunEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="d8556-144">-RunStart</span></span>
<span data-ttu-id="d8556-145">指定使用中視窗執行的開始時間。</span><span class="sxs-lookup"><span data-stu-id="d8556-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="d8556-146">這個 Cmdlet 會取得執行時間落在 *RunStart* 和 *RunEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-147">-上方</span><span class="sxs-lookup"><span data-stu-id="d8556-147">-Top</span></span>
<span data-ttu-id="d8556-148">指定此 Cmdlet 傳回的使用中視窗數目上限。</span><span class="sxs-lookup"><span data-stu-id="d8556-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="d8556-149">-WindowEnd</span></span>
<span data-ttu-id="d8556-150">指定使用中視窗的結束時間。</span><span class="sxs-lookup"><span data-stu-id="d8556-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="d8556-151">這個 Cmdlet 會取得時間落在 *WindowStart* 和 *WindowEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="d8556-152">-WindowStart</span></span>
<span data-ttu-id="d8556-153">指定 [活動] 視窗的開始時間。</span><span class="sxs-lookup"><span data-stu-id="d8556-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="d8556-154">這個 Cmdlet 會取得時間落在 *WindowStart* 和 *WindowEnd* 時間之間的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="d8556-155">-WindowState</span></span>
<span data-ttu-id="d8556-156">指定使用中視窗的狀態。</span><span class="sxs-lookup"><span data-stu-id="d8556-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="d8556-157">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d8556-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8556-158">所有</span><span class="sxs-lookup"><span data-stu-id="d8556-158">None</span></span>
- <span data-ttu-id="d8556-159">等待</span><span class="sxs-lookup"><span data-stu-id="d8556-159">Waiting</span></span>
- <span data-ttu-id="d8556-160">正在</span><span class="sxs-lookup"><span data-stu-id="d8556-160">InProgress</span></span>
- <span data-ttu-id="d8556-161">即可</span><span class="sxs-lookup"><span data-stu-id="d8556-161">Ready</span></span>
- <span data-ttu-id="d8556-162">成功</span><span class="sxs-lookup"><span data-stu-id="d8556-162">Failed</span></span>
- <span data-ttu-id="d8556-163">略過</span><span class="sxs-lookup"><span data-stu-id="d8556-163">Skipped</span></span>

<span data-ttu-id="d8556-164">這個 Cmdlet 會取得此參數指定狀態的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-165">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="d8556-165">-WindowSubstate</span></span>
<span data-ttu-id="d8556-166">指定使用中視窗的子時間。</span><span class="sxs-lookup"><span data-stu-id="d8556-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="d8556-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d8556-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8556-168">取消</span><span class="sxs-lookup"><span data-stu-id="d8556-168">Canceled</span></span>
- <span data-ttu-id="d8556-169">timedOut</span><span class="sxs-lookup"><span data-stu-id="d8556-169">timedOut</span></span>
- <span data-ttu-id="d8556-170">確認</span><span class="sxs-lookup"><span data-stu-id="d8556-170">Validating</span></span>

<span data-ttu-id="d8556-171">這個 Cmdlet 會取得此參數指定之子類型中的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="d8556-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8556-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8556-172">-DefaultProfile</span></span>
<span data-ttu-id="d8556-173">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8556-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8556-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8556-174">CommonParameters</span></span>
<span data-ttu-id="d8556-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8556-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8556-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8556-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8556-177">輸入</span><span class="sxs-lookup"><span data-stu-id="d8556-177">INPUTS</span></span>

## <span data-ttu-id="d8556-178">輸出</span><span class="sxs-lookup"><span data-stu-id="d8556-178">OUTPUTS</span></span>

### <span data-ttu-id="d8556-179">[System.object]。清單 ' 1 [PSActivyWindow，WindowsAzure. WindowsAzure = 0.8.2.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]」）））。</span><span class="sxs-lookup"><span data-stu-id="d8556-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d8556-180">筆記</span><span class="sxs-lookup"><span data-stu-id="d8556-180">NOTES</span></span>

## <span data-ttu-id="d8556-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8556-181">RELATED LINKS</span></span>

[<span data-ttu-id="d8556-182">Azure 資料工廠 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8556-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


