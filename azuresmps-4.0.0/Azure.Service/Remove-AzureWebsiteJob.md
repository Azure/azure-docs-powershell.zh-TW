---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966928"
---
# <span data-ttu-id="e44b4-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e44b4-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="e44b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e44b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e44b4-103">移除網站現有的網頁作業。</span><span class="sxs-lookup"><span data-stu-id="e44b4-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="e44b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e44b4-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e44b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="e44b4-105">DESCRIPTION</span></span>
<span data-ttu-id="e44b4-106">移除網站現有的網頁作業。</span><span class="sxs-lookup"><span data-stu-id="e44b4-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="e44b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="e44b4-107">EXAMPLES</span></span>

### <span data-ttu-id="e44b4-108">範例1：移除網站現有的網頁作業</span><span class="sxs-lookup"><span data-stu-id="e44b4-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="e44b4-109">移除名為 MyWebJob 的 MyWebSite 的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="e44b4-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="e44b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="e44b4-110">PARAMETERS</span></span>

### <span data-ttu-id="e44b4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e44b4-111">-Force</span></span>
<span data-ttu-id="e44b4-112">表示此 Cmdlet 會移除 web 作業，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e44b4-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e44b4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e44b4-113">-JobName</span></span>
<span data-ttu-id="e44b4-114">Web 作業名稱。</span><span class="sxs-lookup"><span data-stu-id="e44b4-114">The web job name.</span></span>

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

### <span data-ttu-id="e44b4-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="e44b4-115">-JobType</span></span>
<span data-ttu-id="e44b4-116">Web 作業類型。</span><span class="sxs-lookup"><span data-stu-id="e44b4-116">The web job type.</span></span>
<span data-ttu-id="e44b4-117">可以觸發或連續使用。</span><span class="sxs-lookup"><span data-stu-id="e44b4-117">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="e44b4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e44b4-118">-Name</span></span>
<span data-ttu-id="e44b4-119">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="e44b4-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="e44b4-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e44b4-120">-Profile</span></span>
<span data-ttu-id="e44b4-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e44b4-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e44b4-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e44b4-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e44b4-123">-槽</span><span class="sxs-lookup"><span data-stu-id="e44b4-123">-Slot</span></span>
<span data-ttu-id="e44b4-124">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="e44b4-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="e44b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44b4-125">CommonParameters</span></span>
<span data-ttu-id="e44b4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e44b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44b4-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e44b4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44b4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e44b4-128">INPUTS</span></span>

## <span data-ttu-id="e44b4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e44b4-129">OUTPUTS</span></span>

## <span data-ttu-id="e44b4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e44b4-130">NOTES</span></span>

## <span data-ttu-id="e44b4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e44b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="e44b4-132">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e44b4-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="e44b4-133">AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e44b4-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="e44b4-134">新-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e44b4-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="e44b4-135">開始-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e44b4-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="e44b4-136">停止 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e44b4-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


