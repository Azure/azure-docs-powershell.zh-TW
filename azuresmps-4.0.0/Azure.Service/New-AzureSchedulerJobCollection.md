---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967426"
---
# <span data-ttu-id="8427a-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8427a-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="8427a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8427a-102">SYNOPSIS</span></span>
<span data-ttu-id="8427a-103">建立排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="8427a-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="8427a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8427a-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8427a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8427a-105">DESCRIPTION</span></span>
<span data-ttu-id="8427a-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8427a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8427a-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="8427a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8427a-108">**新的-AzureSchedulerJobCollection** Cmdlet 會建立排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="8427a-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="8427a-109">如果您沒有指定 *Plan* 參數的值，該 Cmdlet 會建立標準作業集合。</span><span class="sxs-lookup"><span data-stu-id="8427a-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="8427a-110">示例</span><span class="sxs-lookup"><span data-stu-id="8427a-110">EXAMPLES</span></span>

### <span data-ttu-id="8427a-111">範例1：建立包含預設值的排程作業集合</span><span class="sxs-lookup"><span data-stu-id="8427a-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="8427a-112">這個命令會建立名為 JobCollection01 的標準排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="8427a-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="8427a-113">新集合具有標準排程作業集合的預設作業計數和最大週期值。</span><span class="sxs-lookup"><span data-stu-id="8427a-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="8427a-114">範例2：使用指定的值建立排程作業集合</span><span class="sxs-lookup"><span data-stu-id="8427a-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="8427a-115">這個命令會建立名為 JobCollection02 的標準排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="8427a-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="8427a-116">新集合的工作最大作業計數為30個，且每小時最大週期為12次。</span><span class="sxs-lookup"><span data-stu-id="8427a-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="8427a-117">參數</span><span class="sxs-lookup"><span data-stu-id="8427a-117">PARAMETERS</span></span>

### <span data-ttu-id="8427a-118">頻率</span><span class="sxs-lookup"><span data-stu-id="8427a-118">-Frequency</span></span>
<span data-ttu-id="8427a-119">指定可在此排程作業集合中的任何工作上指定的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="8427a-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

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

### <span data-ttu-id="8427a-120">間隔</span><span class="sxs-lookup"><span data-stu-id="8427a-120">-Interval</span></span>
<span data-ttu-id="8427a-121">使用 *frequency* 參數指定的頻率來指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="8427a-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="8427a-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8427a-122">-JobCollectionName</span></span>
<span data-ttu-id="8427a-123">指定新排程作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="8427a-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="8427a-124">-位置</span><span class="sxs-lookup"><span data-stu-id="8427a-124">-Location</span></span>
<span data-ttu-id="8427a-125">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="8427a-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="8427a-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8427a-126">Valid values are:</span></span> 

- <span data-ttu-id="8427a-127">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="8427a-127">Anywhere Asia</span></span>
- <span data-ttu-id="8427a-128">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="8427a-128">Anywhere Europe</span></span>
- <span data-ttu-id="8427a-129">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="8427a-129">Anywhere US</span></span>
- <span data-ttu-id="8427a-130">東亞</span><span class="sxs-lookup"><span data-stu-id="8427a-130">East Asia</span></span>
- <span data-ttu-id="8427a-131">東美國</span><span class="sxs-lookup"><span data-stu-id="8427a-131">East US</span></span>
- <span data-ttu-id="8427a-132">美國中北部</span><span class="sxs-lookup"><span data-stu-id="8427a-132">North Central US</span></span>
- <span data-ttu-id="8427a-133">北歐</span><span class="sxs-lookup"><span data-stu-id="8427a-133">North Europe</span></span>
- <span data-ttu-id="8427a-134">美國中南部</span><span class="sxs-lookup"><span data-stu-id="8427a-134">South Central US</span></span>
- <span data-ttu-id="8427a-135">東南亞</span><span class="sxs-lookup"><span data-stu-id="8427a-135">Southeast Asia</span></span>
- <span data-ttu-id="8427a-136">西歐</span><span class="sxs-lookup"><span data-stu-id="8427a-136">West Europe</span></span>
- <span data-ttu-id="8427a-137">美國西部</span><span class="sxs-lookup"><span data-stu-id="8427a-137">West US</span></span>

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

### <span data-ttu-id="8427a-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8427a-138">-MaxJobCount</span></span>
<span data-ttu-id="8427a-139">指定可在排程作業集合中建立的作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="8427a-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="8427a-140">-方案</span><span class="sxs-lookup"><span data-stu-id="8427a-140">-Plan</span></span>
<span data-ttu-id="8427a-141">指定排程作業集合方案。</span><span class="sxs-lookup"><span data-stu-id="8427a-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="8427a-142">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8427a-142">-Profile</span></span>
<span data-ttu-id="8427a-143">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8427a-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8427a-144">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8427a-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8427a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8427a-145">CommonParameters</span></span>
<span data-ttu-id="8427a-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8427a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8427a-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8427a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8427a-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8427a-148">INPUTS</span></span>

## <span data-ttu-id="8427a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="8427a-149">OUTPUTS</span></span>

## <span data-ttu-id="8427a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="8427a-150">NOTES</span></span>

## <span data-ttu-id="8427a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="8427a-151">RELATED LINKS</span></span>

[<span data-ttu-id="8427a-152">AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8427a-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="8427a-153">移除-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8427a-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="8427a-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8427a-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


