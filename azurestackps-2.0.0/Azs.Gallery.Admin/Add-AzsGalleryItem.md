---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796482"
---
# <span data-ttu-id="8a032-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8a032-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="8a032-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a032-102">SYNOPSIS</span></span>
<span data-ttu-id="8a032-103">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="8a032-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="8a032-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a032-104">SYNTAX</span></span>

### <span data-ttu-id="8a032-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8a032-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a032-106">建立</span><span class="sxs-lookup"><span data-stu-id="8a032-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a032-107">說明</span><span class="sxs-lookup"><span data-stu-id="8a032-107">DESCRIPTION</span></span>
<span data-ttu-id="8a032-108">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="8a032-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="8a032-109">示例</span><span class="sxs-lookup"><span data-stu-id="8a032-109">EXAMPLES</span></span>

### <span data-ttu-id="8a032-110">範例1： Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8a032-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="8a032-111">上傳 TestUbuntu. 1.0.0 到圖庫。</span><span class="sxs-lookup"><span data-stu-id="8a032-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="8a032-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a032-112">PARAMETERS</span></span>

### <span data-ttu-id="8a032-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a032-113">-DefaultProfile</span></span>
<span data-ttu-id="8a032-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a032-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a032-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="8a032-115">-GalleryItemUri</span></span>
<span data-ttu-id="8a032-116">已在線上上傳的圖庫封裝的 URI。</span><span class="sxs-lookup"><span data-stu-id="8a032-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a032-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="8a032-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="8a032-118">畫廊專案負載的位置。</span><span class="sxs-lookup"><span data-stu-id="8a032-118">Location of gallery item payload.</span></span>
<span data-ttu-id="8a032-119">若要建立，請參閱 GALLERYITEMURIPAYLOAD 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8a032-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8a032-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a032-120">-SubscriptionId</span></span>
<span data-ttu-id="8a032-121">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8a032-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a032-122">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8a032-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a032-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8a032-123">-Confirm</span></span>
<span data-ttu-id="8a032-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a032-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a032-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a032-125">-WhatIf</span></span>
<span data-ttu-id="8a032-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a032-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a032-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a032-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a032-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a032-128">CommonParameters</span></span>
<span data-ttu-id="8a032-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a032-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a032-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a032-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a032-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8a032-131">INPUTS</span></span>

### <span data-ttu-id="8a032-132">IGalleryItemUriPayload 中的 [Api20150401] 樣式。</span><span class="sxs-lookup"><span data-stu-id="8a032-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="8a032-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8a032-133">OUTPUTS</span></span>

### <span data-ttu-id="8a032-134">IGalleryItem 中的 [Api20150401] 樣式。</span><span class="sxs-lookup"><span data-stu-id="8a032-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="8a032-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8a032-135">NOTES</span></span>

<span data-ttu-id="8a032-136">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8a032-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a032-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8a032-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8a032-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> ：圖庫專案負載的位置。</span><span class="sxs-lookup"><span data-stu-id="8a032-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="8a032-139">`[GalleryItemUri <String>]`：已在線上上傳的圖庫封裝的 URI。</span><span class="sxs-lookup"><span data-stu-id="8a032-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="8a032-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a032-140">RELATED LINKS</span></span>

