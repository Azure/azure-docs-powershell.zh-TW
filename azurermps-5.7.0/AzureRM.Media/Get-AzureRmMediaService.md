---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624489"
---
# <span data-ttu-id="ffa7e-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="ffa7e-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="ffa7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffa7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa7e-103">取得媒體服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffa7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffa7e-104">SYNTAX</span></span>

### <span data-ttu-id="ffa7e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa7e-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffa7e-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa7e-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa7e-107">說明</span><span class="sxs-lookup"><span data-stu-id="ffa7e-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa7e-108">**AzureRmMediaService** Cmdlet 會取得媒體服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="ffa7e-109">示例</span><span class="sxs-lookup"><span data-stu-id="ffa7e-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa7e-110">範例1：取得資源群組中的所有媒體服務</span><span class="sxs-lookup"><span data-stu-id="ffa7e-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="ffa7e-111">這個命令會取得名為 ResourceGroup001 之資源群組中所有媒體服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="ffa7e-112">範例2：取得媒體服務屬性</span><span class="sxs-lookup"><span data-stu-id="ffa7e-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="ffa7e-113">這個命令會取得屬於名為 ResourceGroup002 之資源群組之名為 MediaService1 的媒體服務屬性。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="ffa7e-114">參數</span><span class="sxs-lookup"><span data-stu-id="ffa7e-114">PARAMETERS</span></span>

### <span data-ttu-id="ffa7e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ffa7e-115">-AccountName</span></span>
<span data-ttu-id="ffa7e-116">指定此 Cmdlet 取得的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa7e-117">-DefaultProfile</span></span>
<span data-ttu-id="ffa7e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ffa7e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffa7e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa7e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ffa7e-120">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa7e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa7e-121">CommonParameters</span></span>
<span data-ttu-id="ffa7e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa7e-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa7e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ffa7e-124">INPUTS</span></span>

### <span data-ttu-id="ffa7e-125">所有</span><span class="sxs-lookup"><span data-stu-id="ffa7e-125">None</span></span>
<span data-ttu-id="ffa7e-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ffa7e-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ffa7e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ffa7e-127">OUTPUTS</span></span>

### <span data-ttu-id="ffa7e-128">PSMediaService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffa7e-128">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="ffa7e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ffa7e-129">NOTES</span></span>

## <span data-ttu-id="ffa7e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffa7e-130">RELATED LINKS</span></span>

[<span data-ttu-id="ffa7e-131">新-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="ffa7e-131">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="ffa7e-132">移除-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="ffa7e-132">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="ffa7e-133">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="ffa7e-133">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


