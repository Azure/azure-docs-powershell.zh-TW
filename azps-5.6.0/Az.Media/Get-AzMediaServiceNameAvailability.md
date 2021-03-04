---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d8928aea539910751c61ad03f5e5a4d67188e371
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904038"
---
# <span data-ttu-id="88562-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="88562-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="88562-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88562-102">SYNOPSIS</span></span>
<span data-ttu-id="88562-103">檢查媒體服務名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="88562-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="88562-104">媒體服務名稱全域都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88562-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="88562-105">語法</span><span class="sxs-lookup"><span data-stu-id="88562-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="88562-106">描述</span><span class="sxs-lookup"><span data-stu-id="88562-106">DESCRIPTION</span></span>
<span data-ttu-id="88562-107">**Get-AzMediaServiceNameAvailability** Cmdlet 會檢查媒體服務名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="88562-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="88562-108">媒體服務名稱全域都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88562-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="88562-109">例子</span><span class="sxs-lookup"><span data-stu-id="88562-109">EXAMPLES</span></span>

### <span data-ttu-id="88562-110">範例 1：檢查媒體服務名稱是否可用</span><span class="sxs-lookup"><span data-stu-id="88562-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="88562-111">此命令會檢查名稱 MediaService1 是否可用。</span><span class="sxs-lookup"><span data-stu-id="88562-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="88562-112">參數</span><span class="sxs-lookup"><span data-stu-id="88562-112">PARAMETERS</span></span>

### <span data-ttu-id="88562-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88562-113">-AccountName</span></span>
<span data-ttu-id="88562-114">指定此 Cmdlet 所獲取的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="88562-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88562-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88562-115">-DefaultProfile</span></span>
<span data-ttu-id="88562-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="88562-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88562-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88562-117">CommonParameters</span></span>
<span data-ttu-id="88562-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88562-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88562-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="88562-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88562-120">輸入</span><span class="sxs-lookup"><span data-stu-id="88562-120">INPUTS</span></span>

### <span data-ttu-id="88562-121">沒有</span><span class="sxs-lookup"><span data-stu-id="88562-121">None</span></span>

## <span data-ttu-id="88562-122">輸出</span><span class="sxs-lookup"><span data-stu-id="88562-122">OUTPUTS</span></span>

### <span data-ttu-id="88562-123">Microsoft.Azure.Commands.Media.models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="88562-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="88562-124">筆記</span><span class="sxs-lookup"><span data-stu-id="88562-124">NOTES</span></span>

## <span data-ttu-id="88562-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="88562-125">RELATED LINKS</span></span>

[<span data-ttu-id="88562-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="88562-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="88562-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="88562-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="88562-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="88562-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="88562-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="88562-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


