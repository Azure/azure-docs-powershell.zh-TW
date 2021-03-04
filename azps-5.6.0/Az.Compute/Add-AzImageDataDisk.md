---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: a5876f705749d1391540bffdf537899e29b9560d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909214"
---
# <span data-ttu-id="3184c-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="3184c-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="3184c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3184c-102">SYNOPSIS</span></span>
<span data-ttu-id="3184c-103">新增資料磁片至影像物件。</span><span class="sxs-lookup"><span data-stu-id="3184c-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="3184c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3184c-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3184c-105">描述</span><span class="sxs-lookup"><span data-stu-id="3184c-105">DESCRIPTION</span></span>
<span data-ttu-id="3184c-106">**Add-AzImageData在** Cmdlet 中新增資料磁片至影像物件。</span><span class="sxs-lookup"><span data-stu-id="3184c-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="3184c-107">例子</span><span class="sxs-lookup"><span data-stu-id="3184c-107">EXAMPLES</span></span>

### <span data-ttu-id="3184c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3184c-108">Example 1</span></span>
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

<span data-ttu-id="3184c-109">第一個命令會建立影像物件，然後將它儲存在$imageConfig變數中。</span><span class="sxs-lookup"><span data-stu-id="3184c-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="3184c-110">接下來三個命令會指派作業系統磁片的路徑和兩個數據磁片$osDiskVhdUri、$dataDiskVhdUri 1 和 $dataDiskVhdUri 2 變數。</span><span class="sxs-lookup"><span data-stu-id="3184c-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="3184c-111">此方法僅適用于下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="3184c-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="3184c-112">接下來三個命令會各自新增一個作業系統磁片和兩個數據磁片至儲存在 $imageConfig。</span><span class="sxs-lookup"><span data-stu-id="3184c-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3184c-113">每個磁片的 URI 會儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 和 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="3184c-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="3184c-114">最後一個命令會建立資源群組 ResourceGroup01 中名為 ImageName01 的影像。</span><span class="sxs-lookup"><span data-stu-id="3184c-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3184c-115">參數</span><span class="sxs-lookup"><span data-stu-id="3184c-115">PARAMETERS</span></span>

### <span data-ttu-id="3184c-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="3184c-116">-BlobUri</span></span>
<span data-ttu-id="3184c-117">指定 Blob 的連結做為 URI。</span><span class="sxs-lookup"><span data-stu-id="3184c-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="3184c-118">-緩存</span><span class="sxs-lookup"><span data-stu-id="3184c-118">-Caching</span></span>
<span data-ttu-id="3184c-119">指定磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="3184c-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="3184c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3184c-120">-DefaultProfile</span></span>
<span data-ttu-id="3184c-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3184c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3184c-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="3184c-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="3184c-123">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3184c-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="3184c-124">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="3184c-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="3184c-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3184c-125">-DiskSizeGB</span></span>
<span data-ttu-id="3184c-126">指定磁片大小 ，以 GB (GB) 。</span><span class="sxs-lookup"><span data-stu-id="3184c-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="3184c-127">-影像</span><span class="sxs-lookup"><span data-stu-id="3184c-127">-Image</span></span>
<span data-ttu-id="3184c-128">指定一個本地影像物件。</span><span class="sxs-lookup"><span data-stu-id="3184c-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="3184c-129">-四分位</span><span class="sxs-lookup"><span data-stu-id="3184c-129">-Lun</span></span>
<span data-ttu-id="3184c-130">指定在中 (單位) 。</span><span class="sxs-lookup"><span data-stu-id="3184c-130">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="3184c-131">-Managed也Id</span><span class="sxs-lookup"><span data-stu-id="3184c-131">-ManagedDiskId</span></span>
<span data-ttu-id="3184c-132">指定受管理磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3184c-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="3184c-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="3184c-133">-SnapshotId</span></span>
<span data-ttu-id="3184c-134">指定快照的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3184c-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="3184c-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3184c-135">-StorageAccountType</span></span>
<span data-ttu-id="3184c-136">資料圖像磁片的儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="3184c-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="3184c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="3184c-137">-Confirm</span></span>
<span data-ttu-id="3184c-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3184c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3184c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3184c-139">-WhatIf</span></span>
<span data-ttu-id="3184c-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3184c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3184c-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3184c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3184c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3184c-142">CommonParameters</span></span>
<span data-ttu-id="3184c-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3184c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3184c-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3184c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3184c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="3184c-145">INPUTS</span></span>

### <span data-ttu-id="3184c-146">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="3184c-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="3184c-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3184c-147">System.Int32</span></span>

### <span data-ttu-id="3184c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3184c-148">System.String</span></span>

### <span data-ttu-id="3184c-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3184c-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3184c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3184c-150">OUTPUTS</span></span>

### <span data-ttu-id="3184c-151">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="3184c-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3184c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3184c-152">NOTES</span></span>

## <span data-ttu-id="3184c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3184c-153">RELATED LINKS</span></span>
