---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967164"
---
# <span data-ttu-id="29e02-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="29e02-101">Add-AzureVhd</span></span>

## <span data-ttu-id="29e02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29e02-102">SYNOPSIS</span></span>
<span data-ttu-id="29e02-103">從內部部署電腦將 VHD 檔案上傳到 Azure 中雲端儲存空間帳戶的 blob。</span><span class="sxs-lookup"><span data-stu-id="29e02-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="29e02-104">句法</span><span class="sxs-lookup"><span data-stu-id="29e02-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="29e02-105">說明</span><span class="sxs-lookup"><span data-stu-id="29e02-105">DESCRIPTION</span></span>
<span data-ttu-id="29e02-106">**AzureVhd** Cmdlet 會在內部部署的虛擬)  (硬碟上傳到 blob 儲存空間帳戶，作為修正的 vhd 映射。</span><span class="sxs-lookup"><span data-stu-id="29e02-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="29e02-107">它具有設定上傳程式的參數，例如，指定將使用的上載程式執行緒數，或覆寫已存在於指定的目標 URI 中的 blob。</span><span class="sxs-lookup"><span data-stu-id="29e02-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="29e02-108">針對內部部署 VHD 影像，也支援修補案例，以便在不需上傳已上傳的基礎映射的情況下，上傳差異磁片影像。</span><span class="sxs-lookup"><span data-stu-id="29e02-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="29e02-109">也支援共用存取簽名 (SAS) URI。</span><span class="sxs-lookup"><span data-stu-id="29e02-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="29e02-110">示例</span><span class="sxs-lookup"><span data-stu-id="29e02-110">EXAMPLES</span></span>

### <span data-ttu-id="29e02-111">範例1：新增 VHD 檔案</span><span class="sxs-lookup"><span data-stu-id="29e02-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="29e02-112">這個命令會將 .vhd 檔案新增至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="29e02-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="29e02-113">範例2：新增 VHD 檔案並覆寫目的地</span><span class="sxs-lookup"><span data-stu-id="29e02-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="29e02-114">這個命令會將 .vhd 檔案新增至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="29e02-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="29e02-115">範例3：新增 VHD 檔案並指定執行緒數</span><span class="sxs-lookup"><span data-stu-id="29e02-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="29e02-116">這個命令會將 .vhd 檔案新增至儲存空間帳戶，並指定要用來上傳檔案的執行緒數。</span><span class="sxs-lookup"><span data-stu-id="29e02-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="29e02-117">範例4：新增 VHD 檔案並指定 SAS URI</span><span class="sxs-lookup"><span data-stu-id="29e02-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="29e02-118">這個命令會將 .vhd 檔案新增至儲存空間帳戶，並指定 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="29e02-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="29e02-119">參數</span><span class="sxs-lookup"><span data-stu-id="29e02-119">PARAMETERS</span></span>

### <span data-ttu-id="29e02-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="29e02-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="29e02-121">指定 Azure Blob 儲存空間中基本映射 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="29e02-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="29e02-122">還支援 URI 輸入中的 SAS。</span><span class="sxs-lookup"><span data-stu-id="29e02-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e02-123">-目的地</span><span class="sxs-lookup"><span data-stu-id="29e02-123">-Destination</span></span>
<span data-ttu-id="29e02-124">指定 Microsoft Azure Blob 儲存空間中的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="29e02-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="29e02-125">支援 URI 輸入中的 SAS。</span><span class="sxs-lookup"><span data-stu-id="29e02-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="29e02-126">不過，在修補案例中，目的地不可以是 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="29e02-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e02-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="29e02-127">-InformationAction</span></span>
<span data-ttu-id="29e02-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="29e02-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="29e02-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="29e02-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29e02-130">持續</span><span class="sxs-lookup"><span data-stu-id="29e02-130">Continue</span></span>
- <span data-ttu-id="29e02-131">理會</span><span class="sxs-lookup"><span data-stu-id="29e02-131">Ignore</span></span>
- <span data-ttu-id="29e02-132">看</span><span class="sxs-lookup"><span data-stu-id="29e02-132">Inquire</span></span>
- <span data-ttu-id="29e02-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29e02-133">SilentlyContinue</span></span>
- <span data-ttu-id="29e02-134">停止</span><span class="sxs-lookup"><span data-stu-id="29e02-134">Stop</span></span>
- <span data-ttu-id="29e02-135">封存</span><span class="sxs-lookup"><span data-stu-id="29e02-135">Suspend</span></span>

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

### <span data-ttu-id="29e02-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29e02-136">-InformationVariable</span></span>
<span data-ttu-id="29e02-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="29e02-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="29e02-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="29e02-138">-LocalFilePath</span></span>
<span data-ttu-id="29e02-139">Species 本地 .vhd 檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="29e02-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e02-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="29e02-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="29e02-141">指定要用於上傳的執行緒數。</span><span class="sxs-lookup"><span data-stu-id="29e02-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e02-142">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="29e02-142">-OverWrite</span></span>
<span data-ttu-id="29e02-143">指定此 Cmdlet 會刪除指定的目標 URI 中現有的 blob （如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="29e02-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e02-144">-設定檔</span><span class="sxs-lookup"><span data-stu-id="29e02-144">-Profile</span></span>
<span data-ttu-id="29e02-145">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="29e02-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29e02-146">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="29e02-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29e02-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e02-147">CommonParameters</span></span>
<span data-ttu-id="29e02-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29e02-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e02-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29e02-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e02-150">輸入</span><span class="sxs-lookup"><span data-stu-id="29e02-150">INPUTS</span></span>

## <span data-ttu-id="29e02-151">輸出</span><span class="sxs-lookup"><span data-stu-id="29e02-151">OUTPUTS</span></span>

## <span data-ttu-id="29e02-152">筆記</span><span class="sxs-lookup"><span data-stu-id="29e02-152">NOTES</span></span>

## <span data-ttu-id="29e02-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="29e02-153">RELATED LINKS</span></span>

[<span data-ttu-id="29e02-154">儲存-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="29e02-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


