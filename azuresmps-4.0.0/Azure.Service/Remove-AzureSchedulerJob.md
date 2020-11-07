---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967575"
---
# <span data-ttu-id="58bc9-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="58bc9-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="58bc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="58bc9-103">刪除排程作業。</span><span class="sxs-lookup"><span data-stu-id="58bc9-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="58bc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="58bc9-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="58bc9-105">說明</span><span class="sxs-lookup"><span data-stu-id="58bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="58bc9-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58bc9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="58bc9-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="58bc9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="58bc9-108">**AzureSchedulerJob** Cmdlet 會刪除排程作業。</span><span class="sxs-lookup"><span data-stu-id="58bc9-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="58bc9-109">示例</span><span class="sxs-lookup"><span data-stu-id="58bc9-109">EXAMPLES</span></span>

### <span data-ttu-id="58bc9-110">範例1：刪除排程作業</span><span class="sxs-lookup"><span data-stu-id="58bc9-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="58bc9-111">這個命令會刪除名為 Job17 的作業。</span><span class="sxs-lookup"><span data-stu-id="58bc9-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="58bc9-112">該作業是名為 JobCollection01 的作業集合的一部分，且位於指定位置。</span><span class="sxs-lookup"><span data-stu-id="58bc9-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="58bc9-113">參數</span><span class="sxs-lookup"><span data-stu-id="58bc9-113">PARAMETERS</span></span>

### <span data-ttu-id="58bc9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="58bc9-114">-Force</span></span>
<span data-ttu-id="58bc9-115">表示此 Cmdlet 會移除排程作業，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58bc9-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="58bc9-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="58bc9-116">-JobCollectionName</span></span>
<span data-ttu-id="58bc9-117">指定包含要刪除之排程作業之集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="58bc9-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="58bc9-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="58bc9-118">-JobName</span></span>
<span data-ttu-id="58bc9-119">指定要刪除的排程作業名稱。</span><span class="sxs-lookup"><span data-stu-id="58bc9-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="58bc9-120">-位置</span><span class="sxs-lookup"><span data-stu-id="58bc9-120">-Location</span></span>
<span data-ttu-id="58bc9-121">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="58bc9-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="58bc9-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="58bc9-122">Valid values are:</span></span> 

- <span data-ttu-id="58bc9-123">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="58bc9-123">Anywhere Asia</span></span>
- <span data-ttu-id="58bc9-124">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="58bc9-124">Anywhere Europe</span></span>
- <span data-ttu-id="58bc9-125">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="58bc9-125">Anywhere US</span></span>
- <span data-ttu-id="58bc9-126">東亞</span><span class="sxs-lookup"><span data-stu-id="58bc9-126">East Asia</span></span>
- <span data-ttu-id="58bc9-127">東美國</span><span class="sxs-lookup"><span data-stu-id="58bc9-127">East US</span></span>
- <span data-ttu-id="58bc9-128">美國中北部</span><span class="sxs-lookup"><span data-stu-id="58bc9-128">North Central US</span></span>
- <span data-ttu-id="58bc9-129">北歐</span><span class="sxs-lookup"><span data-stu-id="58bc9-129">North Europe</span></span>
- <span data-ttu-id="58bc9-130">美國中南部</span><span class="sxs-lookup"><span data-stu-id="58bc9-130">South Central US</span></span>
- <span data-ttu-id="58bc9-131">東南亞</span><span class="sxs-lookup"><span data-stu-id="58bc9-131">Southeast Asia</span></span>
- <span data-ttu-id="58bc9-132">西歐</span><span class="sxs-lookup"><span data-stu-id="58bc9-132">West Europe</span></span>
- <span data-ttu-id="58bc9-133">美國西部</span><span class="sxs-lookup"><span data-stu-id="58bc9-133">West US</span></span>

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

### <span data-ttu-id="58bc9-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="58bc9-134">-Profile</span></span>
<span data-ttu-id="58bc9-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="58bc9-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58bc9-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="58bc9-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58bc9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bc9-137">CommonParameters</span></span>
<span data-ttu-id="58bc9-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58bc9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bc9-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58bc9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bc9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="58bc9-140">INPUTS</span></span>

## <span data-ttu-id="58bc9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="58bc9-141">OUTPUTS</span></span>

## <span data-ttu-id="58bc9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="58bc9-142">NOTES</span></span>

## <span data-ttu-id="58bc9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="58bc9-143">RELATED LINKS</span></span>

[<span data-ttu-id="58bc9-144">AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="58bc9-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


