---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 6e86ed8cde1297af54ffaf8f8c8fbc912da30e69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909190"
---
# <span data-ttu-id="03c7d-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="03c7d-101">Add-AzVhd</span></span>

## <span data-ttu-id="03c7d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="03c7d-103">將虛擬硬碟從內部部署虛擬機器上傳到 Azure 雲端儲存帳戶中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="03c7d-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="03c7d-104">語法</span><span class="sxs-lookup"><span data-stu-id="03c7d-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03c7d-105">描述</span><span class="sxs-lookup"><span data-stu-id="03c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="03c7d-106">**Add-AzVhd** Cmdlet 會以 .vhd 檔案格式將內部部署虛擬硬碟上傳至 Blob 儲存帳戶，作為固定的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="03c7d-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="03c7d-107">您可以設定要使用或覆寫指定目的地 URI 中現有 Blob 的上傳者執行緒數。</span><span class="sxs-lookup"><span data-stu-id="03c7d-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="03c7d-108">另外支援上傳內部部署 .vhd 檔案修補版本的能力。</span><span class="sxs-lookup"><span data-stu-id="03c7d-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="03c7d-109">當基本虛擬硬碟已上傳時，您可以使用基準圖像做為父項上傳不同的磁片。</span><span class="sxs-lookup"><span data-stu-id="03c7d-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="03c7d-110">同時支援 (SAS) URI 的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="03c7d-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="03c7d-111">例子</span><span class="sxs-lookup"><span data-stu-id="03c7d-111">EXAMPLES</span></span>

### <span data-ttu-id="03c7d-112">範例 1：新增 VHD 檔案</span><span class="sxs-lookup"><span data-stu-id="03c7d-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="03c7d-113">此命令會將 .vhd 檔案新增到儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="03c7d-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="03c7d-114">範例 2：新增 VHD 檔案並覆寫目的地</span><span class="sxs-lookup"><span data-stu-id="03c7d-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="03c7d-115">此命令會將 .vhd 檔案新增到儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="03c7d-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="03c7d-116">該命令會覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="03c7d-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="03c7d-117">範例 3：新增 VHD 檔案並指定執行緒數</span><span class="sxs-lookup"><span data-stu-id="03c7d-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="03c7d-118">此命令會將 .vhd 檔案新增到儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="03c7d-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="03c7d-119">命令會指定要用於上傳檔案的執行緒數。</span><span class="sxs-lookup"><span data-stu-id="03c7d-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="03c7d-120">範例 4：新增 VHD 檔案並指定 SAS URI</span><span class="sxs-lookup"><span data-stu-id="03c7d-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="03c7d-121">此命令會將 .vhd 檔案新增到儲存空間帳戶，並指定 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="03c7d-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="03c7d-122">參數</span><span class="sxs-lookup"><span data-stu-id="03c7d-122">PARAMETERS</span></span>

### <span data-ttu-id="03c7d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c7d-123">-AsJob</span></span>
<span data-ttu-id="03c7d-124">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="03c7d-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="03c7d-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="03c7d-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="03c7d-126">指定 Azure Blob 儲存體中基礎圖像 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="03c7d-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="03c7d-127">您可以將 SAS 指定為此參數的值。</span><span class="sxs-lookup"><span data-stu-id="03c7d-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c7d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c7d-128">-DefaultProfile</span></span>
<span data-ttu-id="03c7d-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03c7d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c7d-130">-目的地</span><span class="sxs-lookup"><span data-stu-id="03c7d-130">-Destination</span></span>
<span data-ttu-id="03c7d-131">指定 Blob 儲存體中 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="03c7d-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="03c7d-132">參數支援 SAS URI，雖然修補案例目的地不能是 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="03c7d-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c7d-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="03c7d-133">-LocalFilePath</span></span>
<span data-ttu-id="03c7d-134">指定本地 .vhd 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="03c7d-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c7d-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="03c7d-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="03c7d-136">指定上傳 .vhd 檔案時要使用的上傳者執行緒數。</span><span class="sxs-lookup"><span data-stu-id="03c7d-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c7d-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="03c7d-137">-OverWrite</span></span>
<span data-ttu-id="03c7d-138">表示此 Cmdlet 覆寫指定目的地 URI 中現有的 Blob ，如果有的話。</span><span class="sxs-lookup"><span data-stu-id="03c7d-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c7d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c7d-139">-ResourceGroupName</span></span>
<span data-ttu-id="03c7d-140">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="03c7d-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c7d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c7d-141">CommonParameters</span></span>
<span data-ttu-id="03c7d-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03c7d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c7d-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c7d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c7d-144">輸入</span><span class="sxs-lookup"><span data-stu-id="03c7d-144">INPUTS</span></span>

### <span data-ttu-id="03c7d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="03c7d-145">System.String</span></span>

### <span data-ttu-id="03c7d-146">System.Uri</span><span class="sxs-lookup"><span data-stu-id="03c7d-146">System.Uri</span></span>

### <span data-ttu-id="03c7d-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="03c7d-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="03c7d-148">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03c7d-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03c7d-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03c7d-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03c7d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="03c7d-150">OUTPUTS</span></span>

### <span data-ttu-id="03c7d-151">Microsoft.Azure.Commands.Compute.models.VhdUploadCoNtext</span><span class="sxs-lookup"><span data-stu-id="03c7d-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="03c7d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="03c7d-152">NOTES</span></span>

## <span data-ttu-id="03c7d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="03c7d-153">RELATED LINKS</span></span>

[<span data-ttu-id="03c7d-154">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="03c7d-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


