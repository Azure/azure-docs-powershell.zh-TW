---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968029"
---
# <span data-ttu-id="e2998-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2998-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="e2998-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2998-102">SYNOPSIS</span></span>
<span data-ttu-id="e2998-103">更新影像存放庫中作業系統影像的標籤。</span><span class="sxs-lookup"><span data-stu-id="e2998-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="e2998-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2998-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2998-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2998-105">DESCRIPTION</span></span>
<span data-ttu-id="e2998-106">**更新-AzureVMImage** Cmdlet 會更新影像存放庫中作業系統影像上的標籤。</span><span class="sxs-lookup"><span data-stu-id="e2998-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="e2998-107">它會傳回含有更新影像之資訊的 image 物件。</span><span class="sxs-lookup"><span data-stu-id="e2998-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="e2998-108">示例</span><span class="sxs-lookup"><span data-stu-id="e2998-108">EXAMPLES</span></span>

### <span data-ttu-id="e2998-109">範例1：透過變更圖像標籤來更新影像</span><span class="sxs-lookup"><span data-stu-id="e2998-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="e2998-110">這個命令會將圖像標籤變更為 DoNotUse，以更新名為 Windows-Server-2008-SP2 的影像。</span><span class="sxs-lookup"><span data-stu-id="e2998-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="e2998-111">範例2：依標籤取得所有作業系統，然後更新標籤</span><span class="sxs-lookup"><span data-stu-id="e2998-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="e2998-112">這個命令會取得所有標示為 DoNotUse 的作業系統影像，並將標籤變更為 [更新]。</span><span class="sxs-lookup"><span data-stu-id="e2998-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="e2998-113">參數</span><span class="sxs-lookup"><span data-stu-id="e2998-113">PARAMETERS</span></span>

### <span data-ttu-id="e2998-114">-描述</span><span class="sxs-lookup"><span data-stu-id="e2998-114">-Description</span></span>
<span data-ttu-id="e2998-115">指定作業系統影像的描述。</span><span class="sxs-lookup"><span data-stu-id="e2998-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="e2998-116">-DiskConfig</span></span>
<span data-ttu-id="e2998-117">針對使用 **New-AzureVMImageDiskConfigSet** 、 **AzureVMImageOSDiskConfig** 和 **AzureVMImageDataDiskConfig** Cmdlet 建立的虛擬機器影像，指定作業系統磁片和資料磁片配置。</span><span class="sxs-lookup"><span data-stu-id="e2998-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="e2998-118">-DontShowInGui</span></span>
<span data-ttu-id="e2998-119">表示此 Cmdlet 不會在 GUI 中顯示影像。</span><span class="sxs-lookup"><span data-stu-id="e2998-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-120">-Eula</span><span class="sxs-lookup"><span data-stu-id="e2998-120">-Eula</span></span>
<span data-ttu-id="e2998-121">指定使用者授權合約。</span><span class="sxs-lookup"><span data-stu-id="e2998-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="e2998-122">我們建議值為 URL。</span><span class="sxs-lookup"><span data-stu-id="e2998-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="e2998-123">-IconName</span></span>
<span data-ttu-id="e2998-124">指定作業系統或虛擬機器影像的標準圖示名稱。</span><span class="sxs-lookup"><span data-stu-id="e2998-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="e2998-125">-ImageFamily</span></span>
<span data-ttu-id="e2998-126">指定可用於群組作業系統或虛擬機器影像的值。</span><span class="sxs-lookup"><span data-stu-id="e2998-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e2998-127">-ImageName</span></span>
<span data-ttu-id="e2998-128">指定影像存放庫中要更新的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="e2998-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="e2998-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e2998-129">-InformationAction</span></span>
<span data-ttu-id="e2998-130">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="e2998-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e2998-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e2998-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2998-132">持續</span><span class="sxs-lookup"><span data-stu-id="e2998-132">Continue</span></span>
- <span data-ttu-id="e2998-133">理會</span><span class="sxs-lookup"><span data-stu-id="e2998-133">Ignore</span></span>
- <span data-ttu-id="e2998-134">看</span><span class="sxs-lookup"><span data-stu-id="e2998-134">Inquire</span></span>
- <span data-ttu-id="e2998-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e2998-135">SilentlyContinue</span></span>
- <span data-ttu-id="e2998-136">停止</span><span class="sxs-lookup"><span data-stu-id="e2998-136">Stop</span></span>
- <span data-ttu-id="e2998-137">封存</span><span class="sxs-lookup"><span data-stu-id="e2998-137">Suspend</span></span>

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

### <span data-ttu-id="e2998-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e2998-138">-InformationVariable</span></span>
<span data-ttu-id="e2998-139">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="e2998-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e2998-140">-標籤</span><span class="sxs-lookup"><span data-stu-id="e2998-140">-Label</span></span>
<span data-ttu-id="e2998-141">指定影像的新標籤。</span><span class="sxs-lookup"><span data-stu-id="e2998-141">Specifies the new label of the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-142">-語言</span><span class="sxs-lookup"><span data-stu-id="e2998-142">-Language</span></span>
<span data-ttu-id="e2998-143">指定虛擬機器或作業系統映射中的作業系統語言。</span><span class="sxs-lookup"><span data-stu-id="e2998-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="e2998-144">-PrivacyUri</span></span>
<span data-ttu-id="e2998-145">指定指向檔的 URI，該檔包含與作業系統影像相關的隱私權原則。</span><span class="sxs-lookup"><span data-stu-id="e2998-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-146">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e2998-146">-Profile</span></span>
<span data-ttu-id="e2998-147">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e2998-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2998-148">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e2998-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2998-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="e2998-149">-PublishedDate</span></span>
<span data-ttu-id="e2998-150">指定作業系統影像新增至影像存放庫的日期。</span><span class="sxs-lookup"><span data-stu-id="e2998-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="e2998-151">-RecommendedVMSize</span></span>
<span data-ttu-id="e2998-152">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="e2998-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="e2998-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e2998-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2998-154">深淺</span><span class="sxs-lookup"><span data-stu-id="e2998-154">Medium</span></span>
- <span data-ttu-id="e2998-155">大中型</span><span class="sxs-lookup"><span data-stu-id="e2998-155">Large</span></span>
- <span data-ttu-id="e2998-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="e2998-156">ExtraLarge</span></span>
- <span data-ttu-id="e2998-157">A5</span><span class="sxs-lookup"><span data-stu-id="e2998-157">A5</span></span>
- <span data-ttu-id="e2998-158">A6</span><span class="sxs-lookup"><span data-stu-id="e2998-158">A6</span></span>
- <span data-ttu-id="e2998-159">A7</span><span class="sxs-lookup"><span data-stu-id="e2998-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="e2998-160">-SmallIconName</span></span>
<span data-ttu-id="e2998-161">指定作業系統或虛擬機器影像的小型圖示名稱。</span><span class="sxs-lookup"><span data-stu-id="e2998-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2998-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2998-162">CommonParameters</span></span>
<span data-ttu-id="e2998-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2998-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2998-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2998-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2998-165">輸入</span><span class="sxs-lookup"><span data-stu-id="e2998-165">INPUTS</span></span>

## <span data-ttu-id="e2998-166">輸出</span><span class="sxs-lookup"><span data-stu-id="e2998-166">OUTPUTS</span></span>

### <span data-ttu-id="e2998-167">OSImageCoNtext</span><span class="sxs-lookup"><span data-stu-id="e2998-167">OSImageContext</span></span>

## <span data-ttu-id="e2998-168">筆記</span><span class="sxs-lookup"><span data-stu-id="e2998-168">NOTES</span></span>

## <span data-ttu-id="e2998-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2998-169">RELATED LINKS</span></span>

[<span data-ttu-id="e2998-170">附加 AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2998-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="e2998-171">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2998-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="e2998-172">移除-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2998-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="e2998-173">儲存-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2998-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="e2998-174">新-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e2998-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="e2998-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e2998-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="e2998-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e2998-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


