---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140952"
---
# <span data-ttu-id="b60ac-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="b60ac-101">Add-AzVhd</span></span>

## <span data-ttu-id="b60ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b60ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b60ac-103">將虛擬硬碟從內部部署虛擬機器上傳到 Azure 中雲端儲存空間帳戶的 blob。</span><span class="sxs-lookup"><span data-stu-id="b60ac-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="b60ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="b60ac-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b60ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="b60ac-105">DESCRIPTION</span></span>
<span data-ttu-id="b60ac-106">**AzVhd** Cmdlet 會將內部部署虛擬硬碟（.vhd 檔案格式）上傳到 blob 儲存空間帳戶做為固定虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="b60ac-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="b60ac-107">您可以設定將在指定的目標 URI 中使用或覆寫現有 blob 的上載程式執行緒數。</span><span class="sxs-lookup"><span data-stu-id="b60ac-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="b60ac-108">此外，也支援上傳已修正版本的內部部署 .vhd 檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="b60ac-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="b60ac-109">當基本虛擬硬碟已上傳時，您可以上傳使用基本映射作為父級的差異磁片。</span><span class="sxs-lookup"><span data-stu-id="b60ac-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="b60ac-110">還支援共用存取簽名 (SAS) URI。</span><span class="sxs-lookup"><span data-stu-id="b60ac-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="b60ac-111">示例</span><span class="sxs-lookup"><span data-stu-id="b60ac-111">EXAMPLES</span></span>

### <span data-ttu-id="b60ac-112">範例1：新增 VHD 檔案</span><span class="sxs-lookup"><span data-stu-id="b60ac-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="b60ac-113">這個命令會將 .vhd 檔案新增至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b60ac-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="b60ac-114">範例2：新增 VHD 檔案並覆寫目的地</span><span class="sxs-lookup"><span data-stu-id="b60ac-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="b60ac-115">這個命令會將 .vhd 檔案新增至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b60ac-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="b60ac-116">此命令會覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="b60ac-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="b60ac-117">範例3：新增 VHD 檔案並指定執行緒數</span><span class="sxs-lookup"><span data-stu-id="b60ac-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="b60ac-118">這個命令會將 .vhd 檔案新增至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b60ac-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="b60ac-119">命令會指定要用來上傳檔案的執行緒數。</span><span class="sxs-lookup"><span data-stu-id="b60ac-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="b60ac-120">範例4：新增 VHD 檔案並指定 SAS URI</span><span class="sxs-lookup"><span data-stu-id="b60ac-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="b60ac-121">這個命令會將 .vhd 檔案新增至儲存空間帳戶，並指定 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="b60ac-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="b60ac-122">參數</span><span class="sxs-lookup"><span data-stu-id="b60ac-122">PARAMETERS</span></span>

### <span data-ttu-id="b60ac-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b60ac-123">-AsJob</span></span>
<span data-ttu-id="b60ac-124">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="b60ac-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b60ac-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="b60ac-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="b60ac-126">指定 Azure Blob 儲存空間中基本映射 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="b60ac-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="b60ac-127">您可以將 SAS 指定為此參數的值。</span><span class="sxs-lookup"><span data-stu-id="b60ac-127">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="b60ac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60ac-128">-DefaultProfile</span></span>
<span data-ttu-id="b60ac-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b60ac-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60ac-130">-目的地</span><span class="sxs-lookup"><span data-stu-id="b60ac-130">-Destination</span></span>
<span data-ttu-id="b60ac-131">指定 Blob 儲存區中的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="b60ac-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="b60ac-132">雖然修補案例目的地不能是 SAS URI，但參數支援 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="b60ac-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="b60ac-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="b60ac-133">-LocalFilePath</span></span>
<span data-ttu-id="b60ac-134">指定本機 .vhd 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b60ac-134">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="b60ac-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="b60ac-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="b60ac-136">指定上傳 .vhd 檔案時要使用的上載程式執行緒數。</span><span class="sxs-lookup"><span data-stu-id="b60ac-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="b60ac-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="b60ac-137">-OverWrite</span></span>
<span data-ttu-id="b60ac-138">指示這個 Cmdlet 會覆寫指定的目標 URI （如果有的話）中現有的 blob （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b60ac-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="b60ac-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60ac-139">-ResourceGroupName</span></span>
<span data-ttu-id="b60ac-140">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b60ac-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b60ac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60ac-141">CommonParameters</span></span>
<span data-ttu-id="b60ac-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b60ac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60ac-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b60ac-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60ac-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b60ac-144">INPUTS</span></span>

### <span data-ttu-id="b60ac-145">System.object</span><span class="sxs-lookup"><span data-stu-id="b60ac-145">System.String</span></span>

### <span data-ttu-id="b60ac-146">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="b60ac-146">System.Uri</span></span>

### <span data-ttu-id="b60ac-147">FileInfo</span><span class="sxs-lookup"><span data-stu-id="b60ac-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="b60ac-148">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b60ac-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b60ac-149">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b60ac-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b60ac-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b60ac-150">OUTPUTS</span></span>

### <span data-ttu-id="b60ac-151">VhdUploadCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b60ac-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="b60ac-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b60ac-152">NOTES</span></span>

## <span data-ttu-id="b60ac-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b60ac-153">RELATED LINKS</span></span>

[<span data-ttu-id="b60ac-154">儲存-AzVhd</span><span class="sxs-lookup"><span data-stu-id="b60ac-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


