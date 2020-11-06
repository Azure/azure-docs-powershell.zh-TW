---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 53c9909fb6934e94fc9d0076b73e413856968c8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622829"
---
# <span data-ttu-id="f91cd-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="f91cd-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="f91cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f91cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f91cd-103">將資料磁片新增至影像物件。</span><span class="sxs-lookup"><span data-stu-id="f91cd-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="f91cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="f91cd-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f91cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="f91cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f91cd-106">**AzImageDataDisk** Cmdlet 會將資料磁片新增到 image 物件。</span><span class="sxs-lookup"><span data-stu-id="f91cd-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="f91cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="f91cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f91cd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f91cd-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="f91cd-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="f91cd-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="f91cd-110">接下來的三個命令會將作業系統磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="f91cd-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="f91cd-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="f91cd-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="f91cd-112">接下來的三個命令會將作業系統磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="f91cd-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="f91cd-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="f91cd-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="f91cd-114">最後一個命令會在資源群組 ResourceGroup01 中建立名為 ImageName01 的影像。</span><span class="sxs-lookup"><span data-stu-id="f91cd-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f91cd-115">參數</span><span class="sxs-lookup"><span data-stu-id="f91cd-115">PARAMETERS</span></span>

### <span data-ttu-id="f91cd-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="f91cd-116">-BlobUri</span></span>
<span data-ttu-id="f91cd-117">指定 blob 的連結（作為 URI）。</span><span class="sxs-lookup"><span data-stu-id="f91cd-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-118">-快取</span><span class="sxs-lookup"><span data-stu-id="f91cd-118">-Caching</span></span>
<span data-ttu-id="f91cd-119">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="f91cd-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91cd-120">-DefaultProfile</span></span>
<span data-ttu-id="f91cd-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f91cd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f91cd-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f91cd-122">-DiskSizeGB</span></span>
<span data-ttu-id="f91cd-123">以 Gb (GB) 指定磁片的大小。</span><span class="sxs-lookup"><span data-stu-id="f91cd-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-124">-影像</span><span class="sxs-lookup"><span data-stu-id="f91cd-124">-Image</span></span>
<span data-ttu-id="f91cd-125">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="f91cd-125">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-126">-Lun</span><span class="sxs-lookup"><span data-stu-id="f91cd-126">-Lun</span></span>
<span data-ttu-id="f91cd-127">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="f91cd-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f91cd-128">-ManagedDiskId</span></span>
<span data-ttu-id="f91cd-129">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="f91cd-129">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f91cd-130">-SnapshotId</span></span>
<span data-ttu-id="f91cd-131">指定快照的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f91cd-131">Specifies the ID of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f91cd-132">-StorageAccountType</span></span>
<span data-ttu-id="f91cd-133">資料影像磁片的儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="f91cd-133">The Storage Account type of the data image disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91cd-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f91cd-134">-Confirm</span></span>
<span data-ttu-id="f91cd-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f91cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91cd-136">-WhatIf</span></span>
<span data-ttu-id="f91cd-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f91cd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f91cd-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f91cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91cd-139">CommonParameters</span></span>
<span data-ttu-id="f91cd-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f91cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91cd-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f91cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91cd-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f91cd-142">INPUTS</span></span>

### <span data-ttu-id="f91cd-143">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f91cd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="f91cd-144">System.object</span><span class="sxs-lookup"><span data-stu-id="f91cd-144">System.Int32</span></span>

### <span data-ttu-id="f91cd-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f91cd-145">System.String</span></span>

### <span data-ttu-id="f91cd-146">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="f91cd-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f91cd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="f91cd-147">OUTPUTS</span></span>

### <span data-ttu-id="f91cd-148">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f91cd-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f91cd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="f91cd-149">NOTES</span></span>

## <span data-ttu-id="f91cd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="f91cd-150">RELATED LINKS</span></span>