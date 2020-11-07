---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967756"
---
# <span data-ttu-id="c5ad6-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="c5ad6-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="c5ad6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ad6-103">取得排程作業的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="c5ad6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5ad6-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5ad6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ad6-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c5ad6-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c5ad6-108">**AzureSchedulerJobHistory** Cmdlet 會取得排程作業的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="c5ad6-109">示例</span><span class="sxs-lookup"><span data-stu-id="c5ad6-109">EXAMPLES</span></span>

### <span data-ttu-id="c5ad6-110">範例1：使用其名稱取得作業的歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c5ad6-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="c5ad6-111">這個命令會取得名為 Job01 的工作歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="c5ad6-112">該作業屬於指定位置中名為 JobCollection01 的作業集合。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="c5ad6-113">範例2：使用其名稱取得失敗作業的歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c5ad6-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="c5ad6-114">這個命令會取得名為「Job12」的作業的歷程記錄，其狀態為「失敗」。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="c5ad6-115">該作業屬於指定位置中名為 JobCollection01 的作業集合。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="c5ad6-116">參數</span><span class="sxs-lookup"><span data-stu-id="c5ad6-116">PARAMETERS</span></span>

### <span data-ttu-id="c5ad6-117">-優先</span><span class="sxs-lookup"><span data-stu-id="c5ad6-117">-First</span></span>
<span data-ttu-id="c5ad6-118">只取得指定數目的物件。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="c5ad6-119">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c5ad6-120">-IncludeTotalCount</span></span>
<span data-ttu-id="c5ad6-121">報告資料集中的物件總數 (整數) 接著選取的物件。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="c5ad6-122">如果 Cmdlet 無法判斷總計數，則會顯示「未知總計數」。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="c5ad6-123">這個整數有一個正確性屬性，指出總計數值的可靠性。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="c5ad6-124">精確度的值範圍從0.0 到1.0，其中0.0 表示 Cmdlet 無法計算物件，1.0 表示該計數完全正確，而在0.0 與1.0 之間的值則表示日益可靠的估計。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c5ad6-125">-JobCollectionName</span></span>
<span data-ttu-id="c5ad6-126">指定排程作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="c5ad6-127">這個 Cmdlet 會取得屬於此參數指定之集合之作業的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="c5ad6-128">-JobName</span></span>
<span data-ttu-id="c5ad6-129">指定要取得其歷程記錄的排程作業名稱。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-129">Specifies the name of a scheduler job for which to get the history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="c5ad6-130">-JobStatus</span></span>
<span data-ttu-id="c5ad6-131">指定要取得其歷程記錄的排程作業狀態。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="c5ad6-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c5ad6-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5ad6-133">完畢</span><span class="sxs-lookup"><span data-stu-id="c5ad6-133">Completed</span></span>
- <span data-ttu-id="c5ad6-134">成功</span><span class="sxs-lookup"><span data-stu-id="c5ad6-134">Failed</span></span>

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

### <span data-ttu-id="c5ad6-135">-位置</span><span class="sxs-lookup"><span data-stu-id="c5ad6-135">-Location</span></span>
<span data-ttu-id="c5ad6-136">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="c5ad6-137">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c5ad6-137">Valid values are:</span></span> 

- <span data-ttu-id="c5ad6-138">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="c5ad6-138">Anywhere Asia</span></span>
- <span data-ttu-id="c5ad6-139">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="c5ad6-139">Anywhere Europe</span></span>
- <span data-ttu-id="c5ad6-140">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="c5ad6-140">Anywhere US</span></span>
- <span data-ttu-id="c5ad6-141">東亞</span><span class="sxs-lookup"><span data-stu-id="c5ad6-141">East Asia</span></span>
- <span data-ttu-id="c5ad6-142">東美國</span><span class="sxs-lookup"><span data-stu-id="c5ad6-142">East US</span></span>
- <span data-ttu-id="c5ad6-143">美國中北部</span><span class="sxs-lookup"><span data-stu-id="c5ad6-143">North Central US</span></span>
- <span data-ttu-id="c5ad6-144">北歐</span><span class="sxs-lookup"><span data-stu-id="c5ad6-144">North Europe</span></span>
- <span data-ttu-id="c5ad6-145">美國中南部</span><span class="sxs-lookup"><span data-stu-id="c5ad6-145">South Central US</span></span>
- <span data-ttu-id="c5ad6-146">東南亞</span><span class="sxs-lookup"><span data-stu-id="c5ad6-146">Southeast Asia</span></span>
- <span data-ttu-id="c5ad6-147">西歐</span><span class="sxs-lookup"><span data-stu-id="c5ad6-147">West Europe</span></span>
- <span data-ttu-id="c5ad6-148">美國西部</span><span class="sxs-lookup"><span data-stu-id="c5ad6-148">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-149">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c5ad6-149">-Profile</span></span>
<span data-ttu-id="c5ad6-150">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5ad6-151">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-152">-略過</span><span class="sxs-lookup"><span data-stu-id="c5ad6-152">-Skip</span></span>
<span data-ttu-id="c5ad6-153">忽略指定的物件數目，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="c5ad6-154">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ad6-155">CommonParameters</span></span>
<span data-ttu-id="c5ad6-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ad6-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5ad6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ad6-158">輸入</span><span class="sxs-lookup"><span data-stu-id="c5ad6-158">INPUTS</span></span>

## <span data-ttu-id="c5ad6-159">輸出</span><span class="sxs-lookup"><span data-stu-id="c5ad6-159">OUTPUTS</span></span>

## <span data-ttu-id="c5ad6-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c5ad6-160">NOTES</span></span>

## <span data-ttu-id="c5ad6-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5ad6-161">RELATED LINKS</span></span>

[<span data-ttu-id="c5ad6-162">AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c5ad6-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="c5ad6-163">AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c5ad6-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


