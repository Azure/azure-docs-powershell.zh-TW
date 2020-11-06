---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: ed91cc0c6558797ee1b46070978fe2a41dfb94e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451476"
---
# <span data-ttu-id="fb2bf-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="fb2bf-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="fb2bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2bf-103">檢查是否有可用的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="fb2bf-104">媒體服務名稱是全域唯一的。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb2bf-105">句法</span><span class="sxs-lookup"><span data-stu-id="fb2bf-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="fb2bf-106">說明</span><span class="sxs-lookup"><span data-stu-id="fb2bf-106">DESCRIPTION</span></span>
<span data-ttu-id="fb2bf-107">**AzureRmMediaServiceNameAvailability** Cmdlet 會檢查媒體服務名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="fb2bf-108">媒體服務名稱是全域唯一的。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="fb2bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="fb2bf-109">EXAMPLES</span></span>

### <span data-ttu-id="fb2bf-110">範例1：檢查是否有可用的媒體服務名稱</span><span class="sxs-lookup"><span data-stu-id="fb2bf-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="fb2bf-111">這個命令會檢查是否有可用的名稱 MediaService1。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="fb2bf-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb2bf-112">PARAMETERS</span></span>

### <span data-ttu-id="fb2bf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb2bf-113">-AccountName</span></span>
<span data-ttu-id="fb2bf-114">指定此 Cmdlet 取得的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2bf-115">-DefaultProfile</span></span>
<span data-ttu-id="fb2bf-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fb2bf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2bf-117">CommonParameters</span></span>
<span data-ttu-id="fb2bf-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2bf-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2bf-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fb2bf-120">INPUTS</span></span>

### <span data-ttu-id="fb2bf-121">所有</span><span class="sxs-lookup"><span data-stu-id="fb2bf-121">None</span></span>
<span data-ttu-id="fb2bf-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fb2bf-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb2bf-123">輸出</span><span class="sxs-lookup"><span data-stu-id="fb2bf-123">OUTPUTS</span></span>

### <span data-ttu-id="fb2bf-124">PSCheckNameAvailabilityOutput 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fb2bf-124">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="fb2bf-125">筆記</span><span class="sxs-lookup"><span data-stu-id="fb2bf-125">NOTES</span></span>

## <span data-ttu-id="fb2bf-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb2bf-126">RELATED LINKS</span></span>

[<span data-ttu-id="fb2bf-127">AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb2bf-127">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="fb2bf-128">新-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb2bf-128">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="fb2bf-129">移除-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb2bf-129">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="fb2bf-130">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb2bf-130">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


