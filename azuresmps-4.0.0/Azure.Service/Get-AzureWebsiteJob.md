---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967719"
---
# <span data-ttu-id="cbc5a-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="cbc5a-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="cbc5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc5a-103">取得與網站相關聯的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="cbc5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbc5a-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cbc5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="cbc5a-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc5a-106">取得與網站相關聯的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="cbc5a-107">示例</span><span class="sxs-lookup"><span data-stu-id="cbc5a-107">EXAMPLES</span></span>

### <span data-ttu-id="cbc5a-108">範例1：取得特定的網頁作業資訊</span><span class="sxs-lookup"><span data-stu-id="cbc5a-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="cbc5a-109">從 MyWebsite 生產槽取得名為 MyWebJob 的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="cbc5a-110">範例2：取得網站的所有網頁作業</span><span class="sxs-lookup"><span data-stu-id="cbc5a-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="cbc5a-111">取得與 MyWebsite 生產槽相關聯的所有 web 作業。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="cbc5a-112">範例3：取得所有觸發的 web 作業</span><span class="sxs-lookup"><span data-stu-id="cbc5a-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="cbc5a-113">從 MyWebsite 的分段槽取得所有觸發的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="cbc5a-114">參數</span><span class="sxs-lookup"><span data-stu-id="cbc5a-114">PARAMETERS</span></span>

### <span data-ttu-id="cbc5a-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="cbc5a-115">-JobName</span></span>
<span data-ttu-id="cbc5a-116">Web 作業名稱</span><span class="sxs-lookup"><span data-stu-id="cbc5a-116">The web job name</span></span>

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

### <span data-ttu-id="cbc5a-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="cbc5a-117">-JobType</span></span>
<span data-ttu-id="cbc5a-118">Web 作業類型。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-118">The web job type.</span></span>
<span data-ttu-id="cbc5a-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cbc5a-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbc5a-120">引起</span><span class="sxs-lookup"><span data-stu-id="cbc5a-120">Triggered</span></span>
- <span data-ttu-id="cbc5a-121">連續性</span><span class="sxs-lookup"><span data-stu-id="cbc5a-121">Continuous</span></span>

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

### <span data-ttu-id="cbc5a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbc5a-122">-Name</span></span>
<span data-ttu-id="cbc5a-123">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="cbc5a-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cbc5a-124">-Profile</span></span>
<span data-ttu-id="cbc5a-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbc5a-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cbc5a-127">-槽</span><span class="sxs-lookup"><span data-stu-id="cbc5a-127">-Slot</span></span>
<span data-ttu-id="cbc5a-128">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="cbc5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc5a-129">CommonParameters</span></span>
<span data-ttu-id="cbc5a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc5a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cbc5a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc5a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cbc5a-132">INPUTS</span></span>

## <span data-ttu-id="cbc5a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cbc5a-133">OUTPUTS</span></span>

## <span data-ttu-id="cbc5a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cbc5a-134">NOTES</span></span>

## <span data-ttu-id="cbc5a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbc5a-135">RELATED LINKS</span></span>

[<span data-ttu-id="cbc5a-136">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="cbc5a-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="cbc5a-137">新-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="cbc5a-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="cbc5a-138">移除-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="cbc5a-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="cbc5a-139">開始-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="cbc5a-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="cbc5a-140">停止 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="cbc5a-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


