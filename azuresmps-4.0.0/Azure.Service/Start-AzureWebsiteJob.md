---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967213"
---
# <span data-ttu-id="82494-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="82494-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="82494-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82494-102">SYNOPSIS</span></span>
<span data-ttu-id="82494-103">啟動網站的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="82494-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="82494-104">句法</span><span class="sxs-lookup"><span data-stu-id="82494-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82494-105">說明</span><span class="sxs-lookup"><span data-stu-id="82494-105">DESCRIPTION</span></span>
<span data-ttu-id="82494-106">**Start-AzureWebsiteJob** Cmdlet 會啟動網站的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="82494-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="82494-107">示例</span><span class="sxs-lookup"><span data-stu-id="82494-107">EXAMPLES</span></span>

### <span data-ttu-id="82494-108">範例1：啟動網站的 web 作業</span><span class="sxs-lookup"><span data-stu-id="82494-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="82494-109">啟動名為 MyWebJob 的 MyWebSite 的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="82494-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="82494-110">參數</span><span class="sxs-lookup"><span data-stu-id="82494-110">PARAMETERS</span></span>

### <span data-ttu-id="82494-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="82494-111">-JobName</span></span>
<span data-ttu-id="82494-112">Web 作業名稱。</span><span class="sxs-lookup"><span data-stu-id="82494-112">The web job name.</span></span>

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

### <span data-ttu-id="82494-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="82494-113">-JobType</span></span>
<span data-ttu-id="82494-114">Web 作業類型。</span><span class="sxs-lookup"><span data-stu-id="82494-114">The web job type.</span></span>
<span data-ttu-id="82494-115">可以觸發或連續使用。</span><span class="sxs-lookup"><span data-stu-id="82494-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="82494-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="82494-116">-Name</span></span>
<span data-ttu-id="82494-117">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="82494-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="82494-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82494-118">-PassThru</span></span>
<span data-ttu-id="82494-119">會傳回一個 boolean 值，指出作業已順利啟動。</span><span class="sxs-lookup"><span data-stu-id="82494-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="82494-120">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="82494-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="82494-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="82494-121">-Profile</span></span>
<span data-ttu-id="82494-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="82494-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82494-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="82494-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82494-124">-槽</span><span class="sxs-lookup"><span data-stu-id="82494-124">-Slot</span></span>
<span data-ttu-id="82494-125">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="82494-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="82494-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82494-126">CommonParameters</span></span>
<span data-ttu-id="82494-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82494-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82494-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82494-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82494-129">輸入</span><span class="sxs-lookup"><span data-stu-id="82494-129">INPUTS</span></span>

## <span data-ttu-id="82494-130">輸出</span><span class="sxs-lookup"><span data-stu-id="82494-130">OUTPUTS</span></span>

## <span data-ttu-id="82494-131">筆記</span><span class="sxs-lookup"><span data-stu-id="82494-131">NOTES</span></span>

## <span data-ttu-id="82494-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="82494-132">RELATED LINKS</span></span>

[<span data-ttu-id="82494-133">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="82494-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="82494-134">AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="82494-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="82494-135">新-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="82494-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="82494-136">移除-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="82494-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="82494-137">開始-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="82494-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


