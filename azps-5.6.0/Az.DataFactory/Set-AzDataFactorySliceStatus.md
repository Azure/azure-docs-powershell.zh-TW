---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914054"
---
# <span data-ttu-id="b00c0-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="b00c0-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="b00c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b00c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b00c0-103">在 Azure Data Factory 中設定資料集的區切區狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="b00c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="b00c0-104">SYNTAX</span></span>

### <span data-ttu-id="b00c0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b00c0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b00c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b00c0-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b00c0-107">描述</span><span class="sxs-lookup"><span data-stu-id="b00c0-107">DESCRIPTION</span></span>
<span data-ttu-id="b00c0-108">**Set-AzDataFactorySliceStatus Cmdlet** 會設定 Azure Data Factory 中資料集的區切區狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="b00c0-109">例子</span><span class="sxs-lookup"><span data-stu-id="b00c0-109">EXAMPLES</span></span>

### <span data-ttu-id="b00c0-110">範例 1：設定所有資料區的狀態</span><span class="sxs-lookup"><span data-stu-id="b00c0-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="b00c0-111">此命令會針對名為 DAWikiAggregatedData 的資料集，將所有資料區的狀態設定為在名為 WikiADF 的資料工廠中等待。</span><span class="sxs-lookup"><span data-stu-id="b00c0-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="b00c0-112">*UpdateType* 參數有一個值是一個在一起，因此該命令會設定資料集及所有相依資料集的每一個區段狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="b00c0-113">從屬資料集會做為管道中活動的輸入資料集。</span><span class="sxs-lookup"><span data-stu-id="b00c0-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="b00c0-114">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="b00c0-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="b00c0-115">參數</span><span class="sxs-lookup"><span data-stu-id="b00c0-115">PARAMETERS</span></span>

### <span data-ttu-id="b00c0-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b00c0-116">-DataFactory</span></span>
<span data-ttu-id="b00c0-117">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="b00c0-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b00c0-118">此 Cmdlet 會修改屬於此參數指定之資料工廠的分割區狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b00c0-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b00c0-119">-DataFactoryName</span></span>
<span data-ttu-id="b00c0-120">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b00c0-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b00c0-121">此 Cmdlet 會修改屬於此參數指定之資料工廠的分割區狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b00c0-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="b00c0-122">-DatasetName</span></span>
<span data-ttu-id="b00c0-123">指定此 Cmdlet 修改其資料區之資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b00c0-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="b00c0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00c0-124">-DefaultProfile</span></span>
<span data-ttu-id="b00c0-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b00c0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b00c0-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b00c0-126">-EndDateTime</span></span>
<span data-ttu-id="b00c0-127">將時間週期的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b00c0-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b00c0-128">這次是資料區結尾。</span><span class="sxs-lookup"><span data-stu-id="b00c0-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="b00c0-129">有關 **DateTime** 物件的資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="b00c0-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b00c0-130">*EndDateTime* 必須以 ISO8601 格式指定，如下列範例所示：2015-01-01Z 2015-01T00：00：00Z 2015-01-01T00 ：00：00.000Z (UTC) 2015-01-01T00：00：00：00-08：00 (太平洋標準時間) 預設時區設計工具為 UTC。</span><span class="sxs-lookup"><span data-stu-id="b00c0-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="b00c0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00c0-131">-ResourceGroupName</span></span>
<span data-ttu-id="b00c0-132">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b00c0-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b00c0-133">此 Cmdlet 會修改屬於此參數指定之群組的區區狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b00c0-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b00c0-134">-StartDateTime</span></span>
<span data-ttu-id="b00c0-135">將時間週期的開始指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b00c0-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b00c0-136">這次是資料區開頭。</span><span class="sxs-lookup"><span data-stu-id="b00c0-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="b00c0-137">-狀態</span><span class="sxs-lookup"><span data-stu-id="b00c0-137">-Status</span></span>
<span data-ttu-id="b00c0-138">指定要指派給資料區的狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="b00c0-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b00c0-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b00c0-140">等。</span><span class="sxs-lookup"><span data-stu-id="b00c0-140">Waiting.</span></span>
<span data-ttu-id="b00c0-141">資料區正在等待驗證策略的驗證，然後再進行處理。</span><span class="sxs-lookup"><span data-stu-id="b00c0-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="b00c0-142">準備。</span><span class="sxs-lookup"><span data-stu-id="b00c0-142">Ready.</span></span>
<span data-ttu-id="b00c0-143">資料處理已完成，而且資料區已準備就緒。</span><span class="sxs-lookup"><span data-stu-id="b00c0-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="b00c0-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="b00c0-144">InProgress.</span></span>
<span data-ttu-id="b00c0-145">正在處理資料。</span><span class="sxs-lookup"><span data-stu-id="b00c0-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="b00c0-146">失敗。</span><span class="sxs-lookup"><span data-stu-id="b00c0-146">Failed.</span></span>
<span data-ttu-id="b00c0-147">資料處理失敗。</span><span class="sxs-lookup"><span data-stu-id="b00c0-147">Data processing failed.</span></span>
- <span data-ttu-id="b00c0-148">跳。</span><span class="sxs-lookup"><span data-stu-id="b00c0-148">Skipped.</span></span>
<span data-ttu-id="b00c0-149">略過處理資料區。</span><span class="sxs-lookup"><span data-stu-id="b00c0-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00c0-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="b00c0-150">-UpdateType</span></span>
<span data-ttu-id="b00c0-151">指定該區塊的更新類型。</span><span class="sxs-lookup"><span data-stu-id="b00c0-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="b00c0-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b00c0-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b00c0-153">個人。</span><span class="sxs-lookup"><span data-stu-id="b00c0-153">Individual.</span></span>
<span data-ttu-id="b00c0-154">設定指定時間範圍內資料集的每一個區區狀態。</span><span class="sxs-lookup"><span data-stu-id="b00c0-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="b00c0-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="b00c0-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="b00c0-156">設定資料集及所有相依資料集的每一個區段狀態，以做為管道中活動的輸入資料集。</span><span class="sxs-lookup"><span data-stu-id="b00c0-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00c0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00c0-157">CommonParameters</span></span>
<span data-ttu-id="b00c0-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b00c0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00c0-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b00c0-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00c0-160">輸入</span><span class="sxs-lookup"><span data-stu-id="b00c0-160">INPUTS</span></span>

### <span data-ttu-id="b00c0-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b00c0-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b00c0-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b00c0-162">System.String</span></span>

## <span data-ttu-id="b00c0-163">輸出</span><span class="sxs-lookup"><span data-stu-id="b00c0-163">OUTPUTS</span></span>

### <span data-ttu-id="b00c0-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b00c0-164">System.Boolean</span></span>

## <span data-ttu-id="b00c0-165">筆記</span><span class="sxs-lookup"><span data-stu-id="b00c0-165">NOTES</span></span>
* <span data-ttu-id="b00c0-166">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="b00c0-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b00c0-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="b00c0-167">RELATED LINKS</span></span>

[<span data-ttu-id="b00c0-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="b00c0-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


