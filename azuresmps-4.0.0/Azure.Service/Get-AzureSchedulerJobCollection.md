---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967058"
---
# <span data-ttu-id="db4cd-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="db4cd-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="db4cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="db4cd-103">取得排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="db4cd-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="db4cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="db4cd-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="db4cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="db4cd-105">DESCRIPTION</span></span>
<span data-ttu-id="db4cd-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db4cd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="db4cd-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="db4cd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="db4cd-108">**AzureSchedulerJobCollection** Cmdlet 會取得一或多個排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="db4cd-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="db4cd-109">示例</span><span class="sxs-lookup"><span data-stu-id="db4cd-109">EXAMPLES</span></span>

### <span data-ttu-id="db4cd-110">範例1：取得所有集合</span><span class="sxs-lookup"><span data-stu-id="db4cd-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="db4cd-111">這個命令會取得目前訂閱中所有位置上的所有排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="db4cd-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="db4cd-112">範例2：取得某個位置的所有集合</span><span class="sxs-lookup"><span data-stu-id="db4cd-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="db4cd-113">這個命令會取得名為「中北部」的位置中的所有排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="db4cd-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="db4cd-114">範例3：使用名稱取得集合</span><span class="sxs-lookup"><span data-stu-id="db4cd-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="db4cd-115">這個命令會取得名為 JobCollection01 的排程作業集合。</span><span class="sxs-lookup"><span data-stu-id="db4cd-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="db4cd-116">參數</span><span class="sxs-lookup"><span data-stu-id="db4cd-116">PARAMETERS</span></span>

### <span data-ttu-id="db4cd-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="db4cd-117">-JobCollectionName</span></span>
<span data-ttu-id="db4cd-118">指定要取得的排程作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="db4cd-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="db4cd-119">-位置</span><span class="sxs-lookup"><span data-stu-id="db4cd-119">-Location</span></span>
<span data-ttu-id="db4cd-120">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="db4cd-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="db4cd-121">有效值為：</span><span class="sxs-lookup"><span data-stu-id="db4cd-121">Valid values are:</span></span> 

- <span data-ttu-id="db4cd-122">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="db4cd-122">Anywhere Asia</span></span>
- <span data-ttu-id="db4cd-123">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="db4cd-123">Anywhere Europe</span></span>
- <span data-ttu-id="db4cd-124">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="db4cd-124">Anywhere US</span></span>
- <span data-ttu-id="db4cd-125">東亞</span><span class="sxs-lookup"><span data-stu-id="db4cd-125">East Asia</span></span>
- <span data-ttu-id="db4cd-126">東美國</span><span class="sxs-lookup"><span data-stu-id="db4cd-126">East US</span></span>
- <span data-ttu-id="db4cd-127">美國中北部</span><span class="sxs-lookup"><span data-stu-id="db4cd-127">North Central US</span></span>
- <span data-ttu-id="db4cd-128">北歐</span><span class="sxs-lookup"><span data-stu-id="db4cd-128">North Europe</span></span>
- <span data-ttu-id="db4cd-129">美國中南部</span><span class="sxs-lookup"><span data-stu-id="db4cd-129">South Central US</span></span>
- <span data-ttu-id="db4cd-130">東南亞</span><span class="sxs-lookup"><span data-stu-id="db4cd-130">Southeast Asia</span></span>
- <span data-ttu-id="db4cd-131">西歐</span><span class="sxs-lookup"><span data-stu-id="db4cd-131">West Europe</span></span>
- <span data-ttu-id="db4cd-132">美國西部</span><span class="sxs-lookup"><span data-stu-id="db4cd-132">West US</span></span>

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

### <span data-ttu-id="db4cd-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="db4cd-133">-Profile</span></span>
<span data-ttu-id="db4cd-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="db4cd-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db4cd-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="db4cd-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db4cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4cd-136">CommonParameters</span></span>
<span data-ttu-id="db4cd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db4cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4cd-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db4cd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4cd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="db4cd-139">INPUTS</span></span>

## <span data-ttu-id="db4cd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="db4cd-140">OUTPUTS</span></span>

## <span data-ttu-id="db4cd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="db4cd-141">NOTES</span></span>

## <span data-ttu-id="db4cd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="db4cd-142">RELATED LINKS</span></span>

[<span data-ttu-id="db4cd-143">新-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="db4cd-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="db4cd-144">移除-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="db4cd-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="db4cd-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="db4cd-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


