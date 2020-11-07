---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966907"
---
# <span data-ttu-id="011a6-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="011a6-101">Save-AzureVhd</span></span>

## <span data-ttu-id="011a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="011a6-102">SYNOPSIS</span></span>
<span data-ttu-id="011a6-103">支援下載 .vhd 影像。</span><span class="sxs-lookup"><span data-stu-id="011a6-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="011a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="011a6-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="011a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="011a6-105">DESCRIPTION</span></span>
<span data-ttu-id="011a6-106">**AzureVhd** Cmdlet 可從 blob （儲存在檔案中）下載 .vhd 影像。</span><span class="sxs-lookup"><span data-stu-id="011a6-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="011a6-107">它具有參數以設定下載程式，方法是指定所用的下載程式執行緒數，或覆寫已存在於指定檔案路徑中的檔案。</span><span class="sxs-lookup"><span data-stu-id="011a6-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="011a6-108">[ **儲存-AzureVhd** ] 不會執行任何 VHD 格式轉換，而且會下載 blob。</span><span class="sxs-lookup"><span data-stu-id="011a6-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="011a6-109">示例</span><span class="sxs-lookup"><span data-stu-id="011a6-109">EXAMPLES</span></span>

### <span data-ttu-id="011a6-110">範例1：下載 VHD 檔案</span><span class="sxs-lookup"><span data-stu-id="011a6-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="011a6-111">這個命令會下載 .vhd 檔案。</span><span class="sxs-lookup"><span data-stu-id="011a6-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="011a6-112">範例2：下載 VHD 檔案並覆寫本機檔案</span><span class="sxs-lookup"><span data-stu-id="011a6-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="011a6-113">這個命令會下載 .vhd 檔案，並覆寫目的地路徑中的任何檔案。</span><span class="sxs-lookup"><span data-stu-id="011a6-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="011a6-114">範例3：下載 VHD 檔案並指定執行緒數</span><span class="sxs-lookup"><span data-stu-id="011a6-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="011a6-115">這個命令會下載 .vhd 檔案，並指定執行緒數。</span><span class="sxs-lookup"><span data-stu-id="011a6-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="011a6-116">範例4：下載 VHD 檔案並指定存儲金鑰</span><span class="sxs-lookup"><span data-stu-id="011a6-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="011a6-117">這個命令會下載 .vhd 檔案，並指定存儲金鑰。</span><span class="sxs-lookup"><span data-stu-id="011a6-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="011a6-118">參數</span><span class="sxs-lookup"><span data-stu-id="011a6-118">PARAMETERS</span></span>

### <span data-ttu-id="011a6-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="011a6-119">-InformationAction</span></span>
<span data-ttu-id="011a6-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="011a6-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="011a6-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="011a6-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="011a6-122">持續</span><span class="sxs-lookup"><span data-stu-id="011a6-122">Continue</span></span>
- <span data-ttu-id="011a6-123">理會</span><span class="sxs-lookup"><span data-stu-id="011a6-123">Ignore</span></span>
- <span data-ttu-id="011a6-124">看</span><span class="sxs-lookup"><span data-stu-id="011a6-124">Inquire</span></span>
- <span data-ttu-id="011a6-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="011a6-125">SilentlyContinue</span></span>
- <span data-ttu-id="011a6-126">停止</span><span class="sxs-lookup"><span data-stu-id="011a6-126">Stop</span></span>
- <span data-ttu-id="011a6-127">封存</span><span class="sxs-lookup"><span data-stu-id="011a6-127">Suspend</span></span>

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

### <span data-ttu-id="011a6-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="011a6-128">-InformationVariable</span></span>
<span data-ttu-id="011a6-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="011a6-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="011a6-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="011a6-130">-LocalFilePath</span></span>
<span data-ttu-id="011a6-131">指定本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="011a6-131">Specifies the local file path.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011a6-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="011a6-132">-NumberOfThreads</span></span>
<span data-ttu-id="011a6-133">指定此 Cmdlet 在下載期間使用的下載執行緒數。</span><span class="sxs-lookup"><span data-stu-id="011a6-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011a6-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="011a6-134">-OverWrite</span></span>
<span data-ttu-id="011a6-135">指定此 Cmdlet 會刪除 *LocalFilePath* 檔案所指定的檔案（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="011a6-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="011a6-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="011a6-136">-Profile</span></span>
<span data-ttu-id="011a6-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="011a6-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="011a6-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="011a6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="011a6-139">-來源</span><span class="sxs-lookup"><span data-stu-id="011a6-139">-Source</span></span>
<span data-ttu-id="011a6-140">指定統一資源識別項 (URI) 至中的 blob `Azure` 。</span><span class="sxs-lookup"><span data-stu-id="011a6-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="011a6-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="011a6-141">-StorageKey</span></span>
<span data-ttu-id="011a6-142">指定 [blob 儲存空間] 帳戶的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="011a6-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="011a6-143">如果未提供， **AzureVhd** 會嘗試從 Azure 判斷 *SourceUri* 中帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="011a6-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011a6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011a6-144">CommonParameters</span></span>
<span data-ttu-id="011a6-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="011a6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011a6-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="011a6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011a6-147">輸入</span><span class="sxs-lookup"><span data-stu-id="011a6-147">INPUTS</span></span>

## <span data-ttu-id="011a6-148">輸出</span><span class="sxs-lookup"><span data-stu-id="011a6-148">OUTPUTS</span></span>

## <span data-ttu-id="011a6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="011a6-149">NOTES</span></span>

## <span data-ttu-id="011a6-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="011a6-150">RELATED LINKS</span></span>

[<span data-ttu-id="011a6-151">附加 AzureVhd</span><span class="sxs-lookup"><span data-stu-id="011a6-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


