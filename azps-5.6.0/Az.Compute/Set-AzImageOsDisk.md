---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 79415e5a39703e61843fc58a55ebc4cc5168ef0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916432"
---
# <span data-ttu-id="54f5b-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="54f5b-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="54f5b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="54f5b-103">設定影像物件上的作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="54f5b-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="54f5b-104">語法</span><span class="sxs-lookup"><span data-stu-id="54f5b-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54f5b-105">描述</span><span class="sxs-lookup"><span data-stu-id="54f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="54f5b-106">**Set-AzImageOs以 Cmdlet** 設定影像物件上的作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="54f5b-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="54f5b-107">例子</span><span class="sxs-lookup"><span data-stu-id="54f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="54f5b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="54f5b-108">Example 1</span></span>
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

<span data-ttu-id="54f5b-109">第一個命令會建立影像物件，然後將它儲存在$imageConfig變數中。</span><span class="sxs-lookup"><span data-stu-id="54f5b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="54f5b-110">接下來三個命令會指派 os 磁片的路徑和兩個數據磁片$osDiskVhdUri、$dataDiskVhdUri 1 及$dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="54f5b-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="54f5b-111">此方法僅適用于下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="54f5b-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="54f5b-112">接下來三個命令會各自新增作業系統磁片和兩個數據磁片磁片至儲存在 $imageConfig。</span><span class="sxs-lookup"><span data-stu-id="54f5b-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="54f5b-113">每個磁片的 URI 會儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 和 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="54f5b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="54f5b-114">最後一個命令會建立資源群組 'ResourceGroup01' 中名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="54f5b-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="54f5b-115">參數</span><span class="sxs-lookup"><span data-stu-id="54f5b-115">PARAMETERS</span></span>

### <span data-ttu-id="54f5b-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="54f5b-116">-BlobUri</span></span>
<span data-ttu-id="54f5b-117">指定 Blob 的 Uri。</span><span class="sxs-lookup"><span data-stu-id="54f5b-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f5b-118">-緩存</span><span class="sxs-lookup"><span data-stu-id="54f5b-118">-Caching</span></span>
<span data-ttu-id="54f5b-119">指定磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="54f5b-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f5b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f5b-120">-DefaultProfile</span></span>
<span data-ttu-id="54f5b-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54f5b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f5b-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="54f5b-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="54f5b-123">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="54f5b-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="54f5b-124">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="54f5b-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="54f5b-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="54f5b-125">-DiskSizeGB</span></span>
<span data-ttu-id="54f5b-126">指定磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="54f5b-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="54f5b-127">-影像</span><span class="sxs-lookup"><span data-stu-id="54f5b-127">-Image</span></span>
<span data-ttu-id="54f5b-128">指定一個本地影像物件。</span><span class="sxs-lookup"><span data-stu-id="54f5b-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="54f5b-129">-Managed也Id</span><span class="sxs-lookup"><span data-stu-id="54f5b-129">-ManagedDiskId</span></span>
<span data-ttu-id="54f5b-130">指定受管理磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54f5b-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="54f5b-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="54f5b-131">-OsState</span></span>
<span data-ttu-id="54f5b-132">指定作業系統狀態。</span><span class="sxs-lookup"><span data-stu-id="54f5b-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f5b-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="54f5b-133">-OsType</span></span>
<span data-ttu-id="54f5b-134">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="54f5b-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f5b-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="54f5b-135">-SnapshotId</span></span>
<span data-ttu-id="54f5b-136">指定快照的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54f5b-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="54f5b-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="54f5b-137">-StorageAccountType</span></span>
<span data-ttu-id="54f5b-138">Os 映射磁片的儲存空間帳戶類型</span><span class="sxs-lookup"><span data-stu-id="54f5b-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="54f5b-139">-確認</span><span class="sxs-lookup"><span data-stu-id="54f5b-139">-Confirm</span></span>
<span data-ttu-id="54f5b-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54f5b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f5b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f5b-141">-WhatIf</span></span>
<span data-ttu-id="54f5b-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54f5b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54f5b-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54f5b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f5b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f5b-144">CommonParameters</span></span>
<span data-ttu-id="54f5b-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54f5b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f5b-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54f5b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f5b-147">輸入</span><span class="sxs-lookup"><span data-stu-id="54f5b-147">INPUTS</span></span>

### <span data-ttu-id="54f5b-148">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="54f5b-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="54f5b-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="54f5b-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="54f5b-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="54f5b-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="54f5b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="54f5b-151">System.String</span></span>

### <span data-ttu-id="54f5b-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="54f5b-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="54f5b-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="54f5b-153">System.Int32</span></span>

## <span data-ttu-id="54f5b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="54f5b-154">OUTPUTS</span></span>

### <span data-ttu-id="54f5b-155">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="54f5b-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="54f5b-156">筆記</span><span class="sxs-lookup"><span data-stu-id="54f5b-156">NOTES</span></span>

## <span data-ttu-id="54f5b-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="54f5b-157">RELATED LINKS</span></span>
