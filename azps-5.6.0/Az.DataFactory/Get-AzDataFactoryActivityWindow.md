---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 009f7033b7ecfe26e314a105d0bf88a7433962c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902609"
---
# <span data-ttu-id="492ff-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="492ff-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="492ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="492ff-102">SYNOPSIS</span></span>
<span data-ttu-id="492ff-103">獲得與資料工廠相關聯的使用中視窗相關資訊。</span><span class="sxs-lookup"><span data-stu-id="492ff-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="492ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="492ff-104">SYNTAX</span></span>

### <span data-ttu-id="492ff-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="492ff-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="492ff-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="492ff-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="492ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="492ff-107">DESCRIPTION</span></span>
<span data-ttu-id="492ff-108">**Get-AzDataFactoryActivityWindow** Cmdlet 會取得與資料工廠相關聯的使用中視窗相關資訊。</span><span class="sxs-lookup"><span data-stu-id="492ff-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="492ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="492ff-109">EXAMPLES</span></span>

### <span data-ttu-id="492ff-110">範例 1：取得與資料工廠相關聯的使用中視窗</span><span class="sxs-lookup"><span data-stu-id="492ff-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="492ff-111">此命令會獲得與名為 WikiADF 的資料工廠相關聯的所有使用中視窗相關資訊。</span><span class="sxs-lookup"><span data-stu-id="492ff-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="492ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="492ff-112">PARAMETERS</span></span>

### <span data-ttu-id="492ff-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="492ff-113">-ActivityName</span></span>
<span data-ttu-id="492ff-114">指定活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="492ff-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="492ff-115">此 Cmdlet 會針對此參數指定的活動，獲得使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="492ff-116">-DataFactory</span></span>
<span data-ttu-id="492ff-117">指定 Cmdlet 所返回的 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="492ff-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="492ff-118">此 Cmdlet 會獲得屬於此參數指定之資料工廠的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="492ff-119">-DataFactoryName</span></span>
<span data-ttu-id="492ff-120">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="492ff-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="492ff-121">此 Cmdlet 會獲得屬於此參數指定之資料工廠的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="492ff-122">-DatasetName</span></span>
<span data-ttu-id="492ff-123">指定資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="492ff-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="492ff-124">此 Cmdlet 會獲得屬於此參數指定之資料集的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492ff-125">-DefaultProfile</span></span>
<span data-ttu-id="492ff-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="492ff-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="492ff-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="492ff-127">-Filter</span></span>
<span data-ttu-id="492ff-128">指定使用 Azure 搜尋篩選文法表示的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="492ff-129">有關文法的資訊，請參閱 MSDN 中 Azure 搜尋 (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) 語法。</span><span class="sxs-lookup"><span data-stu-id="492ff-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="492ff-130">使用中視窗清單會根據此參數指定的搜尋字串進行篩選。</span><span class="sxs-lookup"><span data-stu-id="492ff-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="492ff-131">-OrderBy</span></span>
<span data-ttu-id="492ff-132">指定以其中一個使用中視窗清單參數排序回應。</span><span class="sxs-lookup"><span data-stu-id="492ff-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="492ff-133">這是逗號分隔屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="492ff-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="492ff-134">例如：WindowStart、PercentComplete。</span><span class="sxs-lookup"><span data-stu-id="492ff-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="492ff-135">根據預設，順序是 ASC (遞增) 。</span><span class="sxs-lookup"><span data-stu-id="492ff-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="492ff-136">如果您想要以遞減順序排序清單，請指定 DESC。</span><span class="sxs-lookup"><span data-stu-id="492ff-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="492ff-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="492ff-137">-PipelineName</span></span>
<span data-ttu-id="492ff-138">指定管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="492ff-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="492ff-139">此 Cmdlet 會獲得屬於此參數指定之管線的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492ff-140">-ResourceGroupName</span></span>
<span data-ttu-id="492ff-141">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="492ff-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="492ff-142">此 Cmdlet 會獲得屬於此參數指定之資源群組的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="492ff-143">-RunEnd</span></span>
<span data-ttu-id="492ff-144">指定使用中視窗執行結束時間。</span><span class="sxs-lookup"><span data-stu-id="492ff-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="492ff-145">此 Cmdlet 會獲得執行時間落在 *RunStart* 和 *RunEnd 時間之間的活動* 視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="492ff-146">-執行啟動</span><span class="sxs-lookup"><span data-stu-id="492ff-146">-RunStart</span></span>
<span data-ttu-id="492ff-147">指定執行使用中視窗的開始時間。</span><span class="sxs-lookup"><span data-stu-id="492ff-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="492ff-148">此 Cmdlet 會獲得執行時間落在 *RunStart* 和 *RunEnd 時間之間的活動* 視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="492ff-149">-頂端</span><span class="sxs-lookup"><span data-stu-id="492ff-149">-Top</span></span>
<span data-ttu-id="492ff-150">指定此 Cmdlet 會返回的使用中視窗數目上限。</span><span class="sxs-lookup"><span data-stu-id="492ff-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="492ff-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="492ff-151">-WindowEnd</span></span>
<span data-ttu-id="492ff-152">指定使用中視窗的結束時間。</span><span class="sxs-lookup"><span data-stu-id="492ff-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="492ff-153">此 Cmdlet 會獲得時間落在 *WindowsStart* 和 *WindowEnd 時間之間的活動* 視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="492ff-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="492ff-154">-WindowStart</span></span>
<span data-ttu-id="492ff-155">指定使用中視窗的開始時間。</span><span class="sxs-lookup"><span data-stu-id="492ff-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="492ff-156">此 Cmdlet 會獲得時間落在 *WindowsStart* 和 *WindowEnd 時間之間的活動* 視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="492ff-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="492ff-157">-WindowState</span></span>
<span data-ttu-id="492ff-158">指定使用中視窗的狀態。</span><span class="sxs-lookup"><span data-stu-id="492ff-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="492ff-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="492ff-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="492ff-160">沒有</span><span class="sxs-lookup"><span data-stu-id="492ff-160">None</span></span>
- <span data-ttu-id="492ff-161">等</span><span class="sxs-lookup"><span data-stu-id="492ff-161">Waiting</span></span>
- <span data-ttu-id="492ff-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="492ff-162">InProgress</span></span>
- <span data-ttu-id="492ff-163">準備</span><span class="sxs-lookup"><span data-stu-id="492ff-163">Ready</span></span>
- <span data-ttu-id="492ff-164">失敗</span><span class="sxs-lookup"><span data-stu-id="492ff-164">Failed</span></span>
- <span data-ttu-id="492ff-165">略過此 Cmdlet 會獲得此參數指定狀態的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="492ff-166">-WindowSubstate</span></span>
<span data-ttu-id="492ff-167">指定使用中視窗的子狀態。</span><span class="sxs-lookup"><span data-stu-id="492ff-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="492ff-168">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="492ff-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="492ff-169">取消</span><span class="sxs-lookup"><span data-stu-id="492ff-169">Canceled</span></span>
- <span data-ttu-id="492ff-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="492ff-170">timedOut</span></span>
- <span data-ttu-id="492ff-171">驗證此 Cmdlet 會獲得此參數指定的子狀態中的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="492ff-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="492ff-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492ff-172">CommonParameters</span></span>
<span data-ttu-id="492ff-173">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="492ff-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492ff-174">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="492ff-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492ff-175">輸入</span><span class="sxs-lookup"><span data-stu-id="492ff-175">INPUTS</span></span>

### <span data-ttu-id="492ff-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="492ff-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="492ff-177">System.String</span><span class="sxs-lookup"><span data-stu-id="492ff-177">System.String</span></span>

### <span data-ttu-id="492ff-178">System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="492ff-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="492ff-179">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="492ff-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="492ff-180">輸出</span><span class="sxs-lookup"><span data-stu-id="492ff-180">OUTPUTS</span></span>

### <span data-ttu-id="492ff-181">Microsoft.Azure.Commands.DataFactories.models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="492ff-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="492ff-182">筆記</span><span class="sxs-lookup"><span data-stu-id="492ff-182">NOTES</span></span>

## <span data-ttu-id="492ff-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="492ff-183">RELATED LINKS</span></span>

[<span data-ttu-id="492ff-184">Azure DataAzlet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="492ff-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


