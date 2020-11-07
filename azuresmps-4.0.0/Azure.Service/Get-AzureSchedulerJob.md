---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967757"
---
# <span data-ttu-id="4f624-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="4f624-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="4f624-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f624-102">SYNOPSIS</span></span>
<span data-ttu-id="4f624-103">取得排程作業或特定排程作業的清單。</span><span class="sxs-lookup"><span data-stu-id="4f624-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="4f624-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f624-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f624-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f624-105">DESCRIPTION</span></span>
<span data-ttu-id="4f624-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f624-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4f624-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="4f624-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4f624-108">**AzureSchedulerJobCollection** Cmdlet 會取得排程作業或特定排程作業的清單。</span><span class="sxs-lookup"><span data-stu-id="4f624-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="4f624-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f624-109">EXAMPLES</span></span>

### <span data-ttu-id="4f624-110">範例1：取得集合中的所有工作</span><span class="sxs-lookup"><span data-stu-id="4f624-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="4f624-111">這個命令會取得作業集合中名為 JobCollection01 的排程作業。</span><span class="sxs-lookup"><span data-stu-id="4f624-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="4f624-112">範例2：取得已命名的工作</span><span class="sxs-lookup"><span data-stu-id="4f624-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="4f624-113">這個命令會從指定位置中名為 JobCollection01 的集合中取得名為 Job01 的作業。</span><span class="sxs-lookup"><span data-stu-id="4f624-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="4f624-114">範例3：在集合中取得停用的工作</span><span class="sxs-lookup"><span data-stu-id="4f624-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="4f624-115">這個命令會在指定位置中取得屬於 JobCollection01 的所有停用排程作業。</span><span class="sxs-lookup"><span data-stu-id="4f624-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="4f624-116">參數</span><span class="sxs-lookup"><span data-stu-id="4f624-116">PARAMETERS</span></span>

### <span data-ttu-id="4f624-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4f624-117">-JobCollectionName</span></span>
<span data-ttu-id="4f624-118">指定包含要取得之排程作業的集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f624-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="4f624-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="4f624-119">-JobName</span></span>
<span data-ttu-id="4f624-120">指定要取得的排程作業名稱。</span><span class="sxs-lookup"><span data-stu-id="4f624-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="4f624-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="4f624-121">-JobState</span></span>
<span data-ttu-id="4f624-122">指定要取得的排程作業狀態。</span><span class="sxs-lookup"><span data-stu-id="4f624-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="4f624-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4f624-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f624-124">後</span><span class="sxs-lookup"><span data-stu-id="4f624-124">Enabled</span></span>
- <span data-ttu-id="4f624-125">禁止</span><span class="sxs-lookup"><span data-stu-id="4f624-125">Disabled</span></span>
- <span data-ttu-id="4f624-126">錯誤</span><span class="sxs-lookup"><span data-stu-id="4f624-126">Faulted</span></span>
- <span data-ttu-id="4f624-127">完畢</span><span class="sxs-lookup"><span data-stu-id="4f624-127">Completed</span></span>

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

### <span data-ttu-id="4f624-128">-位置</span><span class="sxs-lookup"><span data-stu-id="4f624-128">-Location</span></span>
<span data-ttu-id="4f624-129">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="4f624-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="4f624-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4f624-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f624-131">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="4f624-131">Anywhere Asia</span></span>
- <span data-ttu-id="4f624-132">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="4f624-132">Anywhere Europe</span></span>
- <span data-ttu-id="4f624-133">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="4f624-133">Anywhere US</span></span>
- <span data-ttu-id="4f624-134">東亞</span><span class="sxs-lookup"><span data-stu-id="4f624-134">East Asia</span></span>
- <span data-ttu-id="4f624-135">東美國</span><span class="sxs-lookup"><span data-stu-id="4f624-135">East US</span></span>
- <span data-ttu-id="4f624-136">美國中北部</span><span class="sxs-lookup"><span data-stu-id="4f624-136">North Central US</span></span>
- <span data-ttu-id="4f624-137">北歐</span><span class="sxs-lookup"><span data-stu-id="4f624-137">North Europe</span></span>
- <span data-ttu-id="4f624-138">美國中南部</span><span class="sxs-lookup"><span data-stu-id="4f624-138">South Central US</span></span>
- <span data-ttu-id="4f624-139">東南亞</span><span class="sxs-lookup"><span data-stu-id="4f624-139">Southeast Asia</span></span>
- <span data-ttu-id="4f624-140">西歐</span><span class="sxs-lookup"><span data-stu-id="4f624-140">West Europe</span></span>
- <span data-ttu-id="4f624-141">美國西部</span><span class="sxs-lookup"><span data-stu-id="4f624-141">West US</span></span>

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

### <span data-ttu-id="4f624-142">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4f624-142">-Profile</span></span>
<span data-ttu-id="4f624-143">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4f624-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f624-144">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4f624-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f624-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f624-145">CommonParameters</span></span>
<span data-ttu-id="4f624-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f624-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f624-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f624-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f624-148">輸入</span><span class="sxs-lookup"><span data-stu-id="4f624-148">INPUTS</span></span>

## <span data-ttu-id="4f624-149">輸出</span><span class="sxs-lookup"><span data-stu-id="4f624-149">OUTPUTS</span></span>

## <span data-ttu-id="4f624-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4f624-150">NOTES</span></span>

## <span data-ttu-id="4f624-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f624-151">RELATED LINKS</span></span>

[<span data-ttu-id="4f624-152">移除-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="4f624-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


