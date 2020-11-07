---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966889"
---
# <span data-ttu-id="02e06-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="02e06-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="02e06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02e06-102">SYNOPSIS</span></span>
<span data-ttu-id="02e06-103">更新排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="02e06-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="02e06-104">句法</span><span class="sxs-lookup"><span data-stu-id="02e06-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="02e06-105">說明</span><span class="sxs-lookup"><span data-stu-id="02e06-105">DESCRIPTION</span></span>
<span data-ttu-id="02e06-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02e06-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02e06-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="02e06-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02e06-108">**AzureSchedulerJobCollection** Cmdlet 會更新排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="02e06-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="02e06-109">示例</span><span class="sxs-lookup"><span data-stu-id="02e06-109">EXAMPLES</span></span>

### <span data-ttu-id="02e06-110">範例1：變更集合的最大作業計數</span><span class="sxs-lookup"><span data-stu-id="02e06-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="02e06-111">這個命令會將現有排程作業集合的最大作業計數變更為30（名為 JobCollection01）。</span><span class="sxs-lookup"><span data-stu-id="02e06-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="02e06-112">參數</span><span class="sxs-lookup"><span data-stu-id="02e06-112">PARAMETERS</span></span>

### <span data-ttu-id="02e06-113">頻率</span><span class="sxs-lookup"><span data-stu-id="02e06-113">-Frequency</span></span>
<span data-ttu-id="02e06-114">指定可在此排程作業集合中的任何工作上指定的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="02e06-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="02e06-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="02e06-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02e06-116">數</span><span class="sxs-lookup"><span data-stu-id="02e06-116">Minute</span></span>
- <span data-ttu-id="02e06-117">每</span><span class="sxs-lookup"><span data-stu-id="02e06-117">Hour</span></span>
- <span data-ttu-id="02e06-118">之內</span><span class="sxs-lookup"><span data-stu-id="02e06-118">Day</span></span>
- <span data-ttu-id="02e06-119">周</span><span class="sxs-lookup"><span data-stu-id="02e06-119">Week</span></span>
- <span data-ttu-id="02e06-120">月</span><span class="sxs-lookup"><span data-stu-id="02e06-120">Month</span></span>
- <span data-ttu-id="02e06-121">年</span><span class="sxs-lookup"><span data-stu-id="02e06-121">Year</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e06-122">間隔</span><span class="sxs-lookup"><span data-stu-id="02e06-122">-Interval</span></span>
<span data-ttu-id="02e06-123">使用 *frequency* 參數指定的頻率來指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="02e06-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e06-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="02e06-124">-JobCollectionName</span></span>
<span data-ttu-id="02e06-125">指定要更新的排程作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="02e06-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="02e06-126">-位置</span><span class="sxs-lookup"><span data-stu-id="02e06-126">-Location</span></span>
<span data-ttu-id="02e06-127">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="02e06-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="02e06-128">有效值為：</span><span class="sxs-lookup"><span data-stu-id="02e06-128">Valid values are:</span></span> 

- <span data-ttu-id="02e06-129">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="02e06-129">Anywhere Asia</span></span>
- <span data-ttu-id="02e06-130">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="02e06-130">Anywhere Europe</span></span>
- <span data-ttu-id="02e06-131">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="02e06-131">Anywhere US</span></span>
- <span data-ttu-id="02e06-132">東亞</span><span class="sxs-lookup"><span data-stu-id="02e06-132">East Asia</span></span>
- <span data-ttu-id="02e06-133">東美國</span><span class="sxs-lookup"><span data-stu-id="02e06-133">East US</span></span>
- <span data-ttu-id="02e06-134">美國中北部</span><span class="sxs-lookup"><span data-stu-id="02e06-134">North Central US</span></span>
- <span data-ttu-id="02e06-135">北歐</span><span class="sxs-lookup"><span data-stu-id="02e06-135">North Europe</span></span>
- <span data-ttu-id="02e06-136">美國中南部</span><span class="sxs-lookup"><span data-stu-id="02e06-136">South Central US</span></span>
- <span data-ttu-id="02e06-137">東南亞</span><span class="sxs-lookup"><span data-stu-id="02e06-137">Southeast Asia</span></span>
- <span data-ttu-id="02e06-138">西歐</span><span class="sxs-lookup"><span data-stu-id="02e06-138">West Europe</span></span>
- <span data-ttu-id="02e06-139">美國西部</span><span class="sxs-lookup"><span data-stu-id="02e06-139">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e06-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="02e06-140">-MaxJobCount</span></span>
<span data-ttu-id="02e06-141">指定可在排程作業集合中建立的作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="02e06-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e06-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02e06-142">-PassThru</span></span>
<span data-ttu-id="02e06-143">表示此 Cmdlet 會傳回代表其操作專案的物件。</span><span class="sxs-lookup"><span data-stu-id="02e06-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="02e06-144">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="02e06-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e06-145">-方案</span><span class="sxs-lookup"><span data-stu-id="02e06-145">-Plan</span></span>
<span data-ttu-id="02e06-146">指定排程作業集合方案。</span><span class="sxs-lookup"><span data-stu-id="02e06-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="02e06-147">-設定檔</span><span class="sxs-lookup"><span data-stu-id="02e06-147">-Profile</span></span>
<span data-ttu-id="02e06-148">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="02e06-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02e06-149">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="02e06-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02e06-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e06-150">CommonParameters</span></span>
<span data-ttu-id="02e06-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02e06-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e06-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02e06-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e06-153">輸入</span><span class="sxs-lookup"><span data-stu-id="02e06-153">INPUTS</span></span>

## <span data-ttu-id="02e06-154">輸出</span><span class="sxs-lookup"><span data-stu-id="02e06-154">OUTPUTS</span></span>

## <span data-ttu-id="02e06-155">筆記</span><span class="sxs-lookup"><span data-stu-id="02e06-155">NOTES</span></span>

## <span data-ttu-id="02e06-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="02e06-156">RELATED LINKS</span></span>

[<span data-ttu-id="02e06-157">AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="02e06-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="02e06-158">新-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="02e06-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="02e06-159">移除-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="02e06-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


