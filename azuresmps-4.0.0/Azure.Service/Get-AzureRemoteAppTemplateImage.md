---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968025"
---
# <span data-ttu-id="d2af5-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="d2af5-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="d2af5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2af5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2af5-103">檢索 Azure RemoteApp 範本影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2af5-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="d2af5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2af5-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2af5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2af5-105">DESCRIPTION</span></span>
<span data-ttu-id="d2af5-106">**AzureRemoteAppTemplateImage** Cmdlet 會在 Microsoft Azure 中檢索 Azure RemoteApp 範本影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2af5-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="d2af5-107">這個 Cmdlet 會傳回包含指定範本影像相關資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="d2af5-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="d2af5-108">如果未指定任何範本圖像，則會檢索目前訂閱中所有範本影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2af5-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="d2af5-109">示例</span><span class="sxs-lookup"><span data-stu-id="d2af5-109">EXAMPLES</span></span>

### <span data-ttu-id="d2af5-110">範例1：取得所有範本影像的清單</span><span class="sxs-lookup"><span data-stu-id="d2af5-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="d2af5-111">這個命令會傳回所有範本影像的清單。</span><span class="sxs-lookup"><span data-stu-id="d2af5-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="d2af5-112">範例2：檢索指定範本圖像的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d2af5-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="d2af5-113">這個命令會檢索名為 ContosoApps 的範本影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2af5-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="d2af5-114">參數</span><span class="sxs-lookup"><span data-stu-id="d2af5-114">PARAMETERS</span></span>

### <span data-ttu-id="d2af5-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d2af5-115">-ImageName</span></span>
<span data-ttu-id="d2af5-116">指定 Azure RemoteApp 範本影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2af5-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="d2af5-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d2af5-117">-Profile</span></span>
<span data-ttu-id="d2af5-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d2af5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2af5-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d2af5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2af5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2af5-120">CommonParameters</span></span>
<span data-ttu-id="d2af5-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2af5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2af5-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2af5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2af5-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d2af5-123">INPUTS</span></span>

## <span data-ttu-id="d2af5-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d2af5-124">OUTPUTS</span></span>

## <span data-ttu-id="d2af5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d2af5-125">NOTES</span></span>

## <span data-ttu-id="d2af5-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2af5-126">RELATED LINKS</span></span>

[<span data-ttu-id="d2af5-127">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d2af5-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="d2af5-128">AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="d2af5-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


