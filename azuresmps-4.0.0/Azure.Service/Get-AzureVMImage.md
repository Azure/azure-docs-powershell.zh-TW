---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967978"
---
# <span data-ttu-id="7942d-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7942d-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="7942d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7942d-102">SYNOPSIS</span></span>
<span data-ttu-id="7942d-103">取得其中一個或一組作業系統或影像存放庫中的虛擬機器影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="7942d-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="7942d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7942d-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7942d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7942d-105">DESCRIPTION</span></span>
<span data-ttu-id="7942d-106">**AzureVMImage** Cmdlet 會在一個或多個作業系統清單或影像存放庫中的虛擬機器影像上取得屬性。</span><span class="sxs-lookup"><span data-stu-id="7942d-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="7942d-107">這個 Cmdlet 會傳回存放庫中所有影像的資訊，如果提供其影像名稱，則會傳回特定影像的資訊。</span><span class="sxs-lookup"><span data-stu-id="7942d-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="7942d-108">示例</span><span class="sxs-lookup"><span data-stu-id="7942d-108">EXAMPLES</span></span>

### <span data-ttu-id="7942d-109">範例1：從目前的影像存放庫取得特定影像物件。</span><span class="sxs-lookup"><span data-stu-id="7942d-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="7942d-110">這個命令會從目前的影像存放庫取得名為 Image001 的 image 物件。</span><span class="sxs-lookup"><span data-stu-id="7942d-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="7942d-111">範例2：從目前的影像存放庫取得所有影像</span><span class="sxs-lookup"><span data-stu-id="7942d-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="7942d-112">這個命令會從目前的影像存放庫中檢索所有影像。</span><span class="sxs-lookup"><span data-stu-id="7942d-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="7942d-113">範例3：設定訂閱內容，然後取得所有影像</span><span class="sxs-lookup"><span data-stu-id="7942d-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="7942d-114">這個命令會設定訂閱內容，然後從影像存放庫中檢索所有影像。</span><span class="sxs-lookup"><span data-stu-id="7942d-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="7942d-115">參數</span><span class="sxs-lookup"><span data-stu-id="7942d-115">PARAMETERS</span></span>

### <span data-ttu-id="7942d-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7942d-116">-ImageName</span></span>
<span data-ttu-id="7942d-117">指定影像存放庫中的作業系統或虛擬機器影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="7942d-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="7942d-118">如果您沒有指定此參數，則會傳回所有影像。</span><span class="sxs-lookup"><span data-stu-id="7942d-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7942d-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7942d-119">-InformationAction</span></span>
<span data-ttu-id="7942d-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="7942d-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7942d-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7942d-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7942d-122">持續</span><span class="sxs-lookup"><span data-stu-id="7942d-122">Continue</span></span>
- <span data-ttu-id="7942d-123">理會</span><span class="sxs-lookup"><span data-stu-id="7942d-123">Ignore</span></span>
- <span data-ttu-id="7942d-124">看</span><span class="sxs-lookup"><span data-stu-id="7942d-124">Inquire</span></span>
- <span data-ttu-id="7942d-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7942d-125">SilentlyContinue</span></span>
- <span data-ttu-id="7942d-126">停止</span><span class="sxs-lookup"><span data-stu-id="7942d-126">Stop</span></span>
- <span data-ttu-id="7942d-127">封存</span><span class="sxs-lookup"><span data-stu-id="7942d-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7942d-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7942d-128">-InformationVariable</span></span>
<span data-ttu-id="7942d-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="7942d-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7942d-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7942d-130">-Profile</span></span>
<span data-ttu-id="7942d-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7942d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7942d-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7942d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7942d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7942d-133">CommonParameters</span></span>
<span data-ttu-id="7942d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7942d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7942d-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7942d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7942d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7942d-136">INPUTS</span></span>

## <span data-ttu-id="7942d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="7942d-137">OUTPUTS</span></span>

## <span data-ttu-id="7942d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7942d-138">NOTES</span></span>

## <span data-ttu-id="7942d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7942d-139">RELATED LINKS</span></span>

[<span data-ttu-id="7942d-140">附加 AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7942d-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="7942d-141">移除-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7942d-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="7942d-142">儲存-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7942d-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="7942d-143">更新-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7942d-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


