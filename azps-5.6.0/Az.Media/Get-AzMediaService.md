---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: fcfd642ceaf2f371385ee1f09c99e1efa566941d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916110"
---
# <span data-ttu-id="9725f-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9725f-101">Get-AzMediaService</span></span>

## <span data-ttu-id="9725f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9725f-102">SYNOPSIS</span></span>
<span data-ttu-id="9725f-103">獲得媒體服務相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9725f-103">Gets information about a media service.</span></span>

## <span data-ttu-id="9725f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9725f-104">SYNTAX</span></span>

### <span data-ttu-id="9725f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9725f-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9725f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9725f-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9725f-107">描述</span><span class="sxs-lookup"><span data-stu-id="9725f-107">DESCRIPTION</span></span>
<span data-ttu-id="9725f-108">**Get-AzMediaService** Cmdlet 會取得媒體服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="9725f-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="9725f-109">例子</span><span class="sxs-lookup"><span data-stu-id="9725f-109">EXAMPLES</span></span>

### <span data-ttu-id="9725f-110">範例 1：在資源群組中取得所有媒體服務</span><span class="sxs-lookup"><span data-stu-id="9725f-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="9725f-111">此命令會獲得資源群組中所有媒體服務的屬性，名稱為 ResourceGroup001。</span><span class="sxs-lookup"><span data-stu-id="9725f-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="9725f-112">範例 2：取得媒體服務屬性</span><span class="sxs-lookup"><span data-stu-id="9725f-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="9725f-113">此命令會獲得名為 MediaService1 的媒體服務屬性，該媒體服務屬於名為 ResourceGroup002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9725f-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="9725f-114">參數</span><span class="sxs-lookup"><span data-stu-id="9725f-114">PARAMETERS</span></span>

### <span data-ttu-id="9725f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9725f-115">-AccountName</span></span>
<span data-ttu-id="9725f-116">指定此 Cmdlet 所獲取的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="9725f-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9725f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9725f-117">-DefaultProfile</span></span>
<span data-ttu-id="9725f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9725f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9725f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9725f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9725f-120">指定包含媒體服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9725f-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9725f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9725f-121">CommonParameters</span></span>
<span data-ttu-id="9725f-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9725f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9725f-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9725f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9725f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9725f-124">INPUTS</span></span>

### <span data-ttu-id="9725f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9725f-125">System.String</span></span>

## <span data-ttu-id="9725f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="9725f-126">OUTPUTS</span></span>

### <span data-ttu-id="9725f-127">Microsoft.Azure.Commands.Media.models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="9725f-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="9725f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="9725f-128">NOTES</span></span>

## <span data-ttu-id="9725f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9725f-129">RELATED LINKS</span></span>

[<span data-ttu-id="9725f-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9725f-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="9725f-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9725f-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="9725f-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9725f-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


