---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141530"
---
# <span data-ttu-id="418a6-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="418a6-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="418a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="418a6-102">SYNOPSIS</span></span>
<span data-ttu-id="418a6-103">檢查是否有可用的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="418a6-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="418a6-104">媒體服務名稱是全域唯一的。</span><span class="sxs-lookup"><span data-stu-id="418a6-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="418a6-105">句法</span><span class="sxs-lookup"><span data-stu-id="418a6-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="418a6-106">說明</span><span class="sxs-lookup"><span data-stu-id="418a6-106">DESCRIPTION</span></span>
<span data-ttu-id="418a6-107">**AzMediaServiceNameAvailability** Cmdlet 會檢查媒體服務名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="418a6-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="418a6-108">媒體服務名稱是全域唯一的。</span><span class="sxs-lookup"><span data-stu-id="418a6-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="418a6-109">示例</span><span class="sxs-lookup"><span data-stu-id="418a6-109">EXAMPLES</span></span>

### <span data-ttu-id="418a6-110">範例1：檢查是否有可用的媒體服務名稱</span><span class="sxs-lookup"><span data-stu-id="418a6-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="418a6-111">這個命令會檢查是否有可用的名稱 MediaService1。</span><span class="sxs-lookup"><span data-stu-id="418a6-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="418a6-112">參數</span><span class="sxs-lookup"><span data-stu-id="418a6-112">PARAMETERS</span></span>

### <span data-ttu-id="418a6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="418a6-113">-AccountName</span></span>
<span data-ttu-id="418a6-114">指定此 Cmdlet 取得的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="418a6-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="418a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418a6-115">-DefaultProfile</span></span>
<span data-ttu-id="418a6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="418a6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="418a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418a6-117">CommonParameters</span></span>
<span data-ttu-id="418a6-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="418a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418a6-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="418a6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418a6-120">輸入</span><span class="sxs-lookup"><span data-stu-id="418a6-120">INPUTS</span></span>

### <span data-ttu-id="418a6-121">所有</span><span class="sxs-lookup"><span data-stu-id="418a6-121">None</span></span>

## <span data-ttu-id="418a6-122">輸出</span><span class="sxs-lookup"><span data-stu-id="418a6-122">OUTPUTS</span></span>

### <span data-ttu-id="418a6-123">PSCheckNameAvailabilityOutput 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="418a6-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="418a6-124">筆記</span><span class="sxs-lookup"><span data-stu-id="418a6-124">NOTES</span></span>

## <span data-ttu-id="418a6-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="418a6-125">RELATED LINKS</span></span>

[<span data-ttu-id="418a6-126">AzMediaService</span><span class="sxs-lookup"><span data-stu-id="418a6-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="418a6-127">新-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="418a6-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="418a6-128">移除-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="418a6-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="418a6-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="418a6-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


