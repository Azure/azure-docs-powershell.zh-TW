---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967820"
---
# <span data-ttu-id="8cacd-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="8cacd-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="8cacd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cacd-102">SYNOPSIS</span></span>
<span data-ttu-id="8cacd-103">啟用網站的調試。</span><span class="sxs-lookup"><span data-stu-id="8cacd-103">Enables the website's debug.</span></span>

## <span data-ttu-id="8cacd-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cacd-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8cacd-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cacd-105">DESCRIPTION</span></span>
<span data-ttu-id="8cacd-106">在 Visual Studio 中啟用網站的 [調試] 功能。</span><span class="sxs-lookup"><span data-stu-id="8cacd-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="8cacd-107">示例</span><span class="sxs-lookup"><span data-stu-id="8cacd-107">EXAMPLES</span></span>

### <span data-ttu-id="8cacd-108">啟用 Visual Studio 2013 的調試</span><span class="sxs-lookup"><span data-stu-id="8cacd-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="8cacd-109">啟用 VS 2013 上的調試。</span><span class="sxs-lookup"><span data-stu-id="8cacd-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="8cacd-110">參數</span><span class="sxs-lookup"><span data-stu-id="8cacd-110">PARAMETERS</span></span>

### <span data-ttu-id="8cacd-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="8cacd-111">-Name</span></span>
<span data-ttu-id="8cacd-112">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cacd-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="8cacd-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cacd-113">-PassThru</span></span>
<span data-ttu-id="8cacd-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8cacd-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8cacd-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8cacd-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cacd-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8cacd-116">-Profile</span></span>
<span data-ttu-id="8cacd-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8cacd-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cacd-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8cacd-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8cacd-119">-槽</span><span class="sxs-lookup"><span data-stu-id="8cacd-119">-Slot</span></span>
<span data-ttu-id="8cacd-120">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="8cacd-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="8cacd-121">-版本</span><span class="sxs-lookup"><span data-stu-id="8cacd-121">-Version</span></span>
<span data-ttu-id="8cacd-122">Visual Studio 版本。</span><span class="sxs-lookup"><span data-stu-id="8cacd-122">The Visual Studio version.</span></span>

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

### <span data-ttu-id="8cacd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cacd-123">CommonParameters</span></span>
<span data-ttu-id="8cacd-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cacd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cacd-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cacd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cacd-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8cacd-126">INPUTS</span></span>

## <span data-ttu-id="8cacd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8cacd-127">OUTPUTS</span></span>

## <span data-ttu-id="8cacd-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8cacd-128">NOTES</span></span>

## <span data-ttu-id="8cacd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cacd-129">RELATED LINKS</span></span>

[<span data-ttu-id="8cacd-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="8cacd-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="8cacd-131">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8cacd-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="8cacd-132">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8cacd-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="8cacd-133">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8cacd-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="8cacd-134">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8cacd-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


