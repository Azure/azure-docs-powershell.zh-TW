---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446291"
---
# <span data-ttu-id="88176-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="88176-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="88176-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88176-102">SYNOPSIS</span></span>
<span data-ttu-id="88176-103">在 Azure 資料工廠中設定資料集的扇面狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88176-104">句法</span><span class="sxs-lookup"><span data-stu-id="88176-104">SYNTAX</span></span>

### <span data-ttu-id="88176-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="88176-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88176-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="88176-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88176-107">說明</span><span class="sxs-lookup"><span data-stu-id="88176-107">DESCRIPTION</span></span>
<span data-ttu-id="88176-108">**AzureRmDataFactorySliceStatus** Cmdlet 會設定 Azure 資料工廠中資料集的扇面狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="88176-109">示例</span><span class="sxs-lookup"><span data-stu-id="88176-109">EXAMPLES</span></span>

### <span data-ttu-id="88176-110">範例1：設定所有扇面的狀態</span><span class="sxs-lookup"><span data-stu-id="88176-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="88176-111">這個命令會將名為 DAWikiAggregatedData 的資料集的所有磁區狀態設定為在名為 WikiADF 的資料工廠中等待。</span><span class="sxs-lookup"><span data-stu-id="88176-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="88176-112">*UpdateType* 參數的值為 UpstreamInPipeline，因此命令會針對資料集和所有相依資料集設定每個扇面的狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="88176-113">相依資料集是在管線中作為活動的輸入資料集使用。</span><span class="sxs-lookup"><span data-stu-id="88176-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="88176-114">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="88176-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="88176-115">參數</span><span class="sxs-lookup"><span data-stu-id="88176-115">PARAMETERS</span></span>

### <span data-ttu-id="88176-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="88176-116">-DataFactory</span></span>
<span data-ttu-id="88176-117">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="88176-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="88176-118">這個 Cmdlet 會修改屬於此參數指定之資料工廠的扇面狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="88176-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="88176-119">-DataFactoryName</span></span>
<span data-ttu-id="88176-120">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="88176-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="88176-121">這個 Cmdlet 會修改屬於此參數指定之資料工廠的扇面狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="88176-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="88176-122">-DatasetName</span></span>
<span data-ttu-id="88176-123">指定此 Cmdlet 要修改其扇面的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="88176-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88176-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88176-124">-DefaultProfile</span></span>
<span data-ttu-id="88176-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="88176-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88176-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="88176-126">-EndDateTime</span></span>
<span data-ttu-id="88176-127">將時段的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="88176-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="88176-128">此時間是資料切片的結尾。</span><span class="sxs-lookup"><span data-stu-id="88176-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="88176-129">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="88176-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="88176-130">*EndDateTime* 必須以 ISO8601 格式指定，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="88176-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="88176-131">2015-01-01Z 2015-01-01T00：00： 00Z 2015-01-01T00：00： 00.000 Z (UTC) 2015-01-01T00：00： 00-08： 00 (太平洋標準時間) </span><span class="sxs-lookup"><span data-stu-id="88176-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="88176-132">預設時區指示符為 UTC。</span><span class="sxs-lookup"><span data-stu-id="88176-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88176-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88176-133">-ResourceGroupName</span></span>
<span data-ttu-id="88176-134">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88176-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="88176-135">這個 Cmdlet 會修改屬於此參數指定之群組的扇面狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="88176-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="88176-136">-StartDateTime</span></span>
<span data-ttu-id="88176-137">指定時段的開頭作為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="88176-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="88176-138">此時間是資料切片的開頭。</span><span class="sxs-lookup"><span data-stu-id="88176-138">This time is the beginning of a data slice.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88176-139">-狀態</span><span class="sxs-lookup"><span data-stu-id="88176-139">-Status</span></span>
<span data-ttu-id="88176-140">指定要指派給資料切片的狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="88176-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="88176-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88176-142">等待.</span><span class="sxs-lookup"><span data-stu-id="88176-142">Waiting.</span></span>
<span data-ttu-id="88176-143">資料切片正在等待驗證原則，然後再進行處理。</span><span class="sxs-lookup"><span data-stu-id="88176-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="88176-144">即可.</span><span class="sxs-lookup"><span data-stu-id="88176-144">Ready.</span></span>
<span data-ttu-id="88176-145">資料處理已完成，且資料切片已準備就緒。</span><span class="sxs-lookup"><span data-stu-id="88176-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="88176-146">正在.</span><span class="sxs-lookup"><span data-stu-id="88176-146">InProgress.</span></span>
<span data-ttu-id="88176-147">正在進行資料處理。</span><span class="sxs-lookup"><span data-stu-id="88176-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="88176-148">成功.</span><span class="sxs-lookup"><span data-stu-id="88176-148">Failed.</span></span>
<span data-ttu-id="88176-149">資料處理失敗。</span><span class="sxs-lookup"><span data-stu-id="88176-149">Data processing failed.</span></span>
- <span data-ttu-id="88176-150">略過.</span><span class="sxs-lookup"><span data-stu-id="88176-150">Skipped.</span></span>
<span data-ttu-id="88176-151">已跳過處理資料切片的過程。</span><span class="sxs-lookup"><span data-stu-id="88176-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88176-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="88176-152">-UpdateType</span></span>
<span data-ttu-id="88176-153">指定切片的更新類型。</span><span class="sxs-lookup"><span data-stu-id="88176-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="88176-154">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="88176-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88176-155">某.</span><span class="sxs-lookup"><span data-stu-id="88176-155">Individual.</span></span>
<span data-ttu-id="88176-156">針對指定的時間範圍，設定資料集每個扇面的狀態。</span><span class="sxs-lookup"><span data-stu-id="88176-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="88176-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="88176-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="88176-158">針對資料集和所有相依資料集設定每個磁區的狀態，這些資料集會作為管線中活動的輸入資料集使用。</span><span class="sxs-lookup"><span data-stu-id="88176-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88176-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88176-159">CommonParameters</span></span>
<span data-ttu-id="88176-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88176-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88176-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88176-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88176-162">輸入</span><span class="sxs-lookup"><span data-stu-id="88176-162">INPUTS</span></span>

### <span data-ttu-id="88176-163">所有</span><span class="sxs-lookup"><span data-stu-id="88176-163">None</span></span>
<span data-ttu-id="88176-164">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="88176-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88176-165">輸出</span><span class="sxs-lookup"><span data-stu-id="88176-165">OUTPUTS</span></span>

### <span data-ttu-id="88176-166">System.object</span><span class="sxs-lookup"><span data-stu-id="88176-166">System.Boolean</span></span>

## <span data-ttu-id="88176-167">筆記</span><span class="sxs-lookup"><span data-stu-id="88176-167">NOTES</span></span>
* <span data-ttu-id="88176-168">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="88176-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="88176-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="88176-169">RELATED LINKS</span></span>

[<span data-ttu-id="88176-170">AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="88176-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


