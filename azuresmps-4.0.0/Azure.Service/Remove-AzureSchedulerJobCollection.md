---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967574"
---
# <span data-ttu-id="d4657-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4657-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="d4657-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4657-102">SYNOPSIS</span></span>
<span data-ttu-id="d4657-103">刪除排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="d4657-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="d4657-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4657-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4657-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4657-105">DESCRIPTION</span></span>
<span data-ttu-id="d4657-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4657-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d4657-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="d4657-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d4657-108">**AzureSchedulerJobCollection** Cmdlet 會刪除排程作業集合以及該集合下的任何作業。</span><span class="sxs-lookup"><span data-stu-id="d4657-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="d4657-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4657-109">EXAMPLES</span></span>

### <span data-ttu-id="d4657-110">範例1：刪除某個位置的作業集合</span><span class="sxs-lookup"><span data-stu-id="d4657-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="d4657-111">這個命令會在北中美位置刪除名為 JobCollection01 的排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="d4657-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="d4657-112">此命令也會刪除 [JobCollection01] 下的工作。</span><span class="sxs-lookup"><span data-stu-id="d4657-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="d4657-113">範例2：刪除作業位置</span><span class="sxs-lookup"><span data-stu-id="d4657-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="d4657-114">這個命令會刪除名為 JobCollection02 的排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="d4657-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="d4657-115">此命令也會刪除 [JobCollection02] 下的工作。</span><span class="sxs-lookup"><span data-stu-id="d4657-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="d4657-116">參數</span><span class="sxs-lookup"><span data-stu-id="d4657-116">PARAMETERS</span></span>

### <span data-ttu-id="d4657-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d4657-117">-Force</span></span>
<span data-ttu-id="d4657-118">表示此 Cmdlet 會移除排程作業集合，不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4657-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d4657-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d4657-119">-JobCollectionName</span></span>
<span data-ttu-id="d4657-120">指定要刪除的排程作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4657-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="d4657-121">-位置</span><span class="sxs-lookup"><span data-stu-id="d4657-121">-Location</span></span>
<span data-ttu-id="d4657-122">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="d4657-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="d4657-123">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d4657-123">Valid values are:</span></span> 

- <span data-ttu-id="d4657-124">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="d4657-124">Anywhere Asia</span></span>
- <span data-ttu-id="d4657-125">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="d4657-125">Anywhere Europe</span></span>
- <span data-ttu-id="d4657-126">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="d4657-126">Anywhere US</span></span>
- <span data-ttu-id="d4657-127">東亞</span><span class="sxs-lookup"><span data-stu-id="d4657-127">East Asia</span></span>
- <span data-ttu-id="d4657-128">東美國</span><span class="sxs-lookup"><span data-stu-id="d4657-128">East US</span></span>
- <span data-ttu-id="d4657-129">美國中北部</span><span class="sxs-lookup"><span data-stu-id="d4657-129">North Central US</span></span>
- <span data-ttu-id="d4657-130">北歐</span><span class="sxs-lookup"><span data-stu-id="d4657-130">North Europe</span></span>
- <span data-ttu-id="d4657-131">美國中南部</span><span class="sxs-lookup"><span data-stu-id="d4657-131">South Central US</span></span>
- <span data-ttu-id="d4657-132">東南亞</span><span class="sxs-lookup"><span data-stu-id="d4657-132">Southeast Asia</span></span>
- <span data-ttu-id="d4657-133">西歐</span><span class="sxs-lookup"><span data-stu-id="d4657-133">West Europe</span></span>
- <span data-ttu-id="d4657-134">美國西部</span><span class="sxs-lookup"><span data-stu-id="d4657-134">West US</span></span>

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

### <span data-ttu-id="d4657-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d4657-135">-Profile</span></span>
<span data-ttu-id="d4657-136">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d4657-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4657-137">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d4657-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4657-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4657-138">CommonParameters</span></span>
<span data-ttu-id="d4657-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4657-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4657-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4657-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4657-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d4657-141">INPUTS</span></span>

## <span data-ttu-id="d4657-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d4657-142">OUTPUTS</span></span>

## <span data-ttu-id="d4657-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d4657-143">NOTES</span></span>

## <span data-ttu-id="d4657-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4657-144">RELATED LINKS</span></span>

[<span data-ttu-id="d4657-145">AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4657-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="d4657-146">新-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4657-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="d4657-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4657-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


