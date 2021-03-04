---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 4a88fe1e4bc18aaa31222b2f5d8e2a90629984d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906946"
---
# <span data-ttu-id="08662-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="08662-101">Save-AzVhd</span></span>

## <span data-ttu-id="08662-102">簡介</span><span class="sxs-lookup"><span data-stu-id="08662-102">SYNOPSIS</span></span>
<span data-ttu-id="08662-103">將下載的 .vhd 影像保存在本地。</span><span class="sxs-lookup"><span data-stu-id="08662-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="08662-104">語法</span><span class="sxs-lookup"><span data-stu-id="08662-104">SYNTAX</span></span>

### <span data-ttu-id="08662-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="08662-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08662-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="08662-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08662-107">描述</span><span class="sxs-lookup"><span data-stu-id="08662-107">DESCRIPTION</span></span>
<span data-ttu-id="08662-108">**Save-AzVhd** Cmdlet 會將 .vhd 影像從 Blob 儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="08662-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="08662-109">您可以指定程式使用的下載程式執行緒數目，以及是否要取代已存在的檔案。</span><span class="sxs-lookup"><span data-stu-id="08662-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="08662-110">此 Cmdlet 會直接下載內容。</span><span class="sxs-lookup"><span data-stu-id="08662-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="08662-111">它不適用於任何虛擬硬碟或 VHD (格式) 轉換。</span><span class="sxs-lookup"><span data-stu-id="08662-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="08662-112">例子</span><span class="sxs-lookup"><span data-stu-id="08662-112">EXAMPLES</span></span>

### <span data-ttu-id="08662-113">範例 1：下載影像</span><span class="sxs-lookup"><span data-stu-id="08662-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="08662-114">此命令會下載 .vhd 檔案，並儲存在本地路徑 C：\vhd\Win7Image.vhd 中。</span><span class="sxs-lookup"><span data-stu-id="08662-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="08662-115">範例 2：下載影像並覆寫本地檔案</span><span class="sxs-lookup"><span data-stu-id="08662-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="08662-116">此命令會下載 .vhd 檔案，並儲存在本地路徑中。</span><span class="sxs-lookup"><span data-stu-id="08662-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="08662-117">命令包含 *覆寫* 參數。</span><span class="sxs-lookup"><span data-stu-id="08662-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="08662-118">因此，如果 C：\vhd\Win7Image.vhd 已存在，此命令會取代它。</span><span class="sxs-lookup"><span data-stu-id="08662-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="08662-119">範例 3：使用指定的執行緒數下載影像</span><span class="sxs-lookup"><span data-stu-id="08662-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="08662-120">此命令會下載 .vhd 檔案，並儲存在本地路徑中。</span><span class="sxs-lookup"><span data-stu-id="08662-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="08662-121">此命令會指定 *NumberOfThreads* 參數的值 32。</span><span class="sxs-lookup"><span data-stu-id="08662-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="08662-122">因此，Cmdlet 會為此動作使用 32 個執行緒。</span><span class="sxs-lookup"><span data-stu-id="08662-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="08662-123">範例 4：下載影像並指定儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="08662-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="08662-124">此命令會下載 .vhd 檔案，並指定儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="08662-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="08662-125">參數</span><span class="sxs-lookup"><span data-stu-id="08662-125">PARAMETERS</span></span>

### <span data-ttu-id="08662-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08662-126">-AsJob</span></span>
<span data-ttu-id="08662-127">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="08662-127">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08662-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08662-128">-DefaultProfile</span></span>
<span data-ttu-id="08662-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="08662-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08662-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="08662-130">-LocalFilePath</span></span>
<span data-ttu-id="08662-131">指定已儲存圖像的本地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="08662-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08662-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="08662-132">-NumberOfThreads</span></span>
<span data-ttu-id="08662-133">指定此 Cmdlet 在下載期間使用的下載執行緒數。</span><span class="sxs-lookup"><span data-stu-id="08662-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08662-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="08662-134">-OverWrite</span></span>
<span data-ttu-id="08662-135">表示此 Cmdlet 取代 *LocalFilePath* 檔案指定的檔案 ，如果檔案存在的話。</span><span class="sxs-lookup"><span data-stu-id="08662-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08662-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08662-136">-ResourceGroupName</span></span>
<span data-ttu-id="08662-137">指定儲存帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="08662-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08662-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="08662-138">-SourceUri</span></span>
<span data-ttu-id="08662-139">指定中 blob (URI) 統一資源識別項 `Azure` 。</span><span class="sxs-lookup"><span data-stu-id="08662-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08662-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="08662-140">-StorageKey</span></span>
<span data-ttu-id="08662-141">指定 Blob 儲存帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="08662-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="08662-142">如果您未指定金鑰，此 Cmdlet 會嘗試從 Azure 判斷 *SourceUri* 中帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="08662-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08662-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08662-143">CommonParameters</span></span>
<span data-ttu-id="08662-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="08662-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08662-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08662-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08662-146">輸入</span><span class="sxs-lookup"><span data-stu-id="08662-146">INPUTS</span></span>

### <span data-ttu-id="08662-147">System.String</span><span class="sxs-lookup"><span data-stu-id="08662-147">System.String</span></span>

### <span data-ttu-id="08662-148">System.Uri</span><span class="sxs-lookup"><span data-stu-id="08662-148">System.Uri</span></span>

## <span data-ttu-id="08662-149">輸出</span><span class="sxs-lookup"><span data-stu-id="08662-149">OUTPUTS</span></span>

### <span data-ttu-id="08662-150">Microsoft.Azure.Commands.Compute.models.VhdDownloadCoNtext</span><span class="sxs-lookup"><span data-stu-id="08662-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="08662-151">筆記</span><span class="sxs-lookup"><span data-stu-id="08662-151">NOTES</span></span>

## <span data-ttu-id="08662-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="08662-152">RELATED LINKS</span></span>

[<span data-ttu-id="08662-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="08662-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


