---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967161"
---
# <span data-ttu-id="bea52-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="bea52-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="bea52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bea52-102">SYNOPSIS</span></span>
<span data-ttu-id="bea52-103">將新的作業系統映射或新的虛擬機器影像新增至影像存放庫。</span><span class="sxs-lookup"><span data-stu-id="bea52-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="bea52-104">句法</span><span class="sxs-lookup"><span data-stu-id="bea52-104">SYNTAX</span></span>

### <span data-ttu-id="bea52-105">OSImage (預設) </span><span class="sxs-lookup"><span data-stu-id="bea52-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bea52-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="bea52-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bea52-107">說明</span><span class="sxs-lookup"><span data-stu-id="bea52-107">DESCRIPTION</span></span>
<span data-ttu-id="bea52-108">**AzureVMImage** Cmdlet 會將新的作業系統映射或新的虛擬機器影像新增至影像存放庫。</span><span class="sxs-lookup"><span data-stu-id="bea52-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="bea52-109">此影像是通用的作業系統影像，使用 Windows 版 Sysprep 或 Linux 的使用適當工具進行發佈。</span><span class="sxs-lookup"><span data-stu-id="bea52-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="bea52-110">示例</span><span class="sxs-lookup"><span data-stu-id="bea52-110">EXAMPLES</span></span>

### <span data-ttu-id="bea52-111">範例1：在知識庫中新增作業系統映射</span><span class="sxs-lookup"><span data-stu-id="bea52-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="bea52-112">這個範例會將作業系統影像新增至儲存庫。</span><span class="sxs-lookup"><span data-stu-id="bea52-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="bea52-113">參數</span><span class="sxs-lookup"><span data-stu-id="bea52-113">PARAMETERS</span></span>

### <span data-ttu-id="bea52-114">-描述</span><span class="sxs-lookup"><span data-stu-id="bea52-114">-Description</span></span>
<span data-ttu-id="bea52-115">指定作業系統影像的描述。</span><span class="sxs-lookup"><span data-stu-id="bea52-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="bea52-116">-DiskConfig</span></span>
<span data-ttu-id="bea52-117">指定虛擬機器影像的作業系統磁片設定。</span><span class="sxs-lookup"><span data-stu-id="bea52-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-118">-Eula</span><span class="sxs-lookup"><span data-stu-id="bea52-118">-Eula</span></span>
<span data-ttu-id="bea52-119">指定使用者授權合約。</span><span class="sxs-lookup"><span data-stu-id="bea52-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="bea52-120">建議您針對此值使用 URL。</span><span class="sxs-lookup"><span data-stu-id="bea52-120">It is recommended that you use an URL for this value.</span></span>

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

### <span data-ttu-id="bea52-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="bea52-121">-IconName</span></span>
<span data-ttu-id="bea52-122">指定將影像新增至儲存庫時所使用之圖示的名稱。</span><span class="sxs-lookup"><span data-stu-id="bea52-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

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

### <span data-ttu-id="bea52-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="bea52-123">-ImageFamily</span></span>
<span data-ttu-id="bea52-124">指定用於群組作業系統影像的值。</span><span class="sxs-lookup"><span data-stu-id="bea52-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="bea52-125">-ImageName</span></span>
<span data-ttu-id="bea52-126">指定要新增至影像存放庫的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="bea52-126">Specifies the name of the image being added to the image repository.</span></span>

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

### <span data-ttu-id="bea52-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bea52-127">-InformationAction</span></span>
<span data-ttu-id="bea52-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="bea52-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bea52-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bea52-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bea52-130">持續</span><span class="sxs-lookup"><span data-stu-id="bea52-130">Continue</span></span>
- <span data-ttu-id="bea52-131">理會</span><span class="sxs-lookup"><span data-stu-id="bea52-131">Ignore</span></span>
- <span data-ttu-id="bea52-132">看</span><span class="sxs-lookup"><span data-stu-id="bea52-132">Inquire</span></span>
- <span data-ttu-id="bea52-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bea52-133">SilentlyContinue</span></span>
- <span data-ttu-id="bea52-134">停止</span><span class="sxs-lookup"><span data-stu-id="bea52-134">Stop</span></span>
- <span data-ttu-id="bea52-135">封存</span><span class="sxs-lookup"><span data-stu-id="bea52-135">Suspend</span></span>

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

### <span data-ttu-id="bea52-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bea52-136">-InformationVariable</span></span>
<span data-ttu-id="bea52-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="bea52-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bea52-138">-標籤</span><span class="sxs-lookup"><span data-stu-id="bea52-138">-Label</span></span>
<span data-ttu-id="bea52-139">指定要提供影像的標籤。</span><span class="sxs-lookup"><span data-stu-id="bea52-139">Specifies a label to give the image.</span></span>

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

### <span data-ttu-id="bea52-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="bea52-140">-MediaLocation</span></span>
<span data-ttu-id="bea52-141">指定影像所在之物理 blob 頁面的位置。</span><span class="sxs-lookup"><span data-stu-id="bea52-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="bea52-142">這是目前訂閱儲存空間中 blob 頁面的連結。</span><span class="sxs-lookup"><span data-stu-id="bea52-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-143">-OS</span><span class="sxs-lookup"><span data-stu-id="bea52-143">-OS</span></span>
<span data-ttu-id="bea52-144">指定影像的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="bea52-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="bea52-145">-PrivacyUri</span></span>
<span data-ttu-id="bea52-146">指定指向檔的 URL，該檔包含與作業系統影像相關的隱私權原則。</span><span class="sxs-lookup"><span data-stu-id="bea52-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-147">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bea52-147">-Profile</span></span>
<span data-ttu-id="bea52-148">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bea52-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bea52-149">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bea52-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bea52-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="bea52-150">-PublishedDate</span></span>
<span data-ttu-id="bea52-151">指定作業系統影像新增至影像存放庫的日期。</span><span class="sxs-lookup"><span data-stu-id="bea52-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea52-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="bea52-152">-RecommendedVMSize</span></span>
<span data-ttu-id="bea52-153">指定從作業系統映射建立的虛擬機器所要使用的大小。</span><span class="sxs-lookup"><span data-stu-id="bea52-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="bea52-154">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bea52-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bea52-155">深淺</span><span class="sxs-lookup"><span data-stu-id="bea52-155">Medium</span></span>
- <span data-ttu-id="bea52-156">大中型</span><span class="sxs-lookup"><span data-stu-id="bea52-156">Large</span></span>
- <span data-ttu-id="bea52-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="bea52-157">ExtraLarge</span></span>
- <span data-ttu-id="bea52-158">A5</span><span class="sxs-lookup"><span data-stu-id="bea52-158">A5</span></span>
- <span data-ttu-id="bea52-159">A6</span><span class="sxs-lookup"><span data-stu-id="bea52-159">A6</span></span>
- <span data-ttu-id="bea52-160">A7</span><span class="sxs-lookup"><span data-stu-id="bea52-160">A7</span></span>

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

### <span data-ttu-id="bea52-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="bea52-161">-ShowInGui</span></span>
<span data-ttu-id="bea52-162">表示此 Cmdlet 在 GUI 中顯示影像。</span><span class="sxs-lookup"><span data-stu-id="bea52-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

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

### <span data-ttu-id="bea52-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="bea52-163">-SmallIconName</span></span>
<span data-ttu-id="bea52-164">指定將影像新增至儲存庫時所使用的小圖示名稱。</span><span class="sxs-lookup"><span data-stu-id="bea52-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

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

### <span data-ttu-id="bea52-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea52-165">CommonParameters</span></span>
<span data-ttu-id="bea52-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bea52-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea52-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bea52-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea52-168">輸入</span><span class="sxs-lookup"><span data-stu-id="bea52-168">INPUTS</span></span>

## <span data-ttu-id="bea52-169">輸出</span><span class="sxs-lookup"><span data-stu-id="bea52-169">OUTPUTS</span></span>

### <span data-ttu-id="bea52-170">OSImageCoNtext</span><span class="sxs-lookup"><span data-stu-id="bea52-170">OSImageContext</span></span>

## <span data-ttu-id="bea52-171">筆記</span><span class="sxs-lookup"><span data-stu-id="bea52-171">NOTES</span></span>

## <span data-ttu-id="bea52-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="bea52-172">RELATED LINKS</span></span>

[<span data-ttu-id="bea52-173">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="bea52-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="bea52-174">移除-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="bea52-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="bea52-175">儲存-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="bea52-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="bea52-176">更新-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="bea52-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


