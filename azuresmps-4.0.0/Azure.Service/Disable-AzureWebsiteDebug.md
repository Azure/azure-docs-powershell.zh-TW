---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967137"
---
# <span data-ttu-id="f84e8-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="f84e8-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="f84e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f84e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f84e8-103">停用網站的調試。</span><span class="sxs-lookup"><span data-stu-id="f84e8-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="f84e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f84e8-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f84e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="f84e8-105">DESCRIPTION</span></span>
<span data-ttu-id="f84e8-106">在 Visual Studio 中停用網站的調試。</span><span class="sxs-lookup"><span data-stu-id="f84e8-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="f84e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="f84e8-107">EXAMPLES</span></span>

### <span data-ttu-id="f84e8-108">--------------停用網站調試--------------</span><span class="sxs-lookup"><span data-stu-id="f84e8-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="f84e8-109">在網站 MyWebsite 上停用網站調試</span><span class="sxs-lookup"><span data-stu-id="f84e8-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="f84e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="f84e8-110">PARAMETERS</span></span>

### <span data-ttu-id="f84e8-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="f84e8-111">-Name</span></span>
<span data-ttu-id="f84e8-112">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="f84e8-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="f84e8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f84e8-113">-PassThru</span></span>
<span data-ttu-id="f84e8-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f84e8-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f84e8-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f84e8-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f84e8-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f84e8-116">-Profile</span></span>
<span data-ttu-id="f84e8-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f84e8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f84e8-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f84e8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f84e8-119">-槽</span><span class="sxs-lookup"><span data-stu-id="f84e8-119">-Slot</span></span>
<span data-ttu-id="f84e8-120">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="f84e8-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="f84e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84e8-121">CommonParameters</span></span>
<span data-ttu-id="f84e8-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f84e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84e8-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f84e8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84e8-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f84e8-124">INPUTS</span></span>

## <span data-ttu-id="f84e8-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f84e8-125">OUTPUTS</span></span>

## <span data-ttu-id="f84e8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f84e8-126">NOTES</span></span>

## <span data-ttu-id="f84e8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f84e8-127">RELATED LINKS</span></span>

[<span data-ttu-id="f84e8-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="f84e8-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="f84e8-129">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f84e8-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="f84e8-130">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f84e8-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="f84e8-131">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f84e8-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="f84e8-132">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f84e8-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


