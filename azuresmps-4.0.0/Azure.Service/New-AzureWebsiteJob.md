---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967629"
---
# <span data-ttu-id="0ad16-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0ad16-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="0ad16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ad16-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad16-103">建立網站的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="0ad16-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="0ad16-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ad16-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ad16-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ad16-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad16-106">**新的-AzureWebsiteJob** Cmdlet 會建立網站的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="0ad16-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="0ad16-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ad16-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad16-108">範例1：建立網站的新網頁作業</span><span class="sxs-lookup"><span data-stu-id="0ad16-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="0ad16-109">建立連續作業來呼叫網站 MyWebsite 上的 job.bat。</span><span class="sxs-lookup"><span data-stu-id="0ad16-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="0ad16-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ad16-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad16-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="0ad16-111">-JobFile</span></span>
<span data-ttu-id="0ad16-112">網頁作業檔案。</span><span class="sxs-lookup"><span data-stu-id="0ad16-112">The web job file.</span></span>

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

### <span data-ttu-id="0ad16-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0ad16-113">-JobName</span></span>
<span data-ttu-id="0ad16-114">Web 作業名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad16-114">The web job name.</span></span>

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

### <span data-ttu-id="0ad16-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="0ad16-115">-JobType</span></span>
<span data-ttu-id="0ad16-116">Web 作業類型。</span><span class="sxs-lookup"><span data-stu-id="0ad16-116">The web job type.</span></span>
<span data-ttu-id="0ad16-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0ad16-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ad16-118">引起</span><span class="sxs-lookup"><span data-stu-id="0ad16-118">Triggered</span></span> 
- <span data-ttu-id="0ad16-119">連續性</span><span class="sxs-lookup"><span data-stu-id="0ad16-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad16-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ad16-120">-Name</span></span>
<span data-ttu-id="0ad16-121">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad16-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="0ad16-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0ad16-122">-Profile</span></span>
<span data-ttu-id="0ad16-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0ad16-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ad16-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0ad16-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ad16-125">-槽</span><span class="sxs-lookup"><span data-stu-id="0ad16-125">-Slot</span></span>
<span data-ttu-id="0ad16-126">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad16-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="0ad16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad16-127">CommonParameters</span></span>
<span data-ttu-id="0ad16-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ad16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad16-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ad16-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad16-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0ad16-130">INPUTS</span></span>

## <span data-ttu-id="0ad16-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0ad16-131">OUTPUTS</span></span>

## <span data-ttu-id="0ad16-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0ad16-132">NOTES</span></span>

## <span data-ttu-id="0ad16-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ad16-133">RELATED LINKS</span></span>

[<span data-ttu-id="0ad16-134">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0ad16-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0ad16-135">AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0ad16-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="0ad16-136">移除-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0ad16-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="0ad16-137">開始-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0ad16-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="0ad16-138">停止 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0ad16-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


