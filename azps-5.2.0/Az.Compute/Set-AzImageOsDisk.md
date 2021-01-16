---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284419"
---
# <span data-ttu-id="7f975-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="7f975-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="7f975-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f975-102">SYNOPSIS</span></span>
<span data-ttu-id="7f975-103">在 image 物件上設定作業系統的磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="7f975-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="7f975-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f975-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f975-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f975-105">DESCRIPTION</span></span>
<span data-ttu-id="7f975-106">**AzImageOsDisk** Cmdlet 會在 image 物件上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="7f975-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="7f975-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f975-107">EXAMPLES</span></span>

### <span data-ttu-id="7f975-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7f975-108">Example 1</span></span>
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

<span data-ttu-id="7f975-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f975-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="7f975-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="7f975-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="7f975-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="7f975-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="7f975-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="7f975-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="7f975-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="7f975-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="7f975-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="7f975-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7f975-115">參數</span><span class="sxs-lookup"><span data-stu-id="7f975-115">PARAMETERS</span></span>

### <span data-ttu-id="7f975-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="7f975-116">-BlobUri</span></span>
<span data-ttu-id="7f975-117">指定 blob 的 Uri。</span><span class="sxs-lookup"><span data-stu-id="7f975-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="7f975-118">-快取</span><span class="sxs-lookup"><span data-stu-id="7f975-118">-Caching</span></span>
<span data-ttu-id="7f975-119">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="7f975-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="7f975-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f975-120">-DefaultProfile</span></span>
<span data-ttu-id="7f975-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f975-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f975-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7f975-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="7f975-123">指定客戶管理磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f975-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="7f975-124">只能為受管理的磁片指定這種情況。</span><span class="sxs-lookup"><span data-stu-id="7f975-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="7f975-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7f975-125">-DiskSizeGB</span></span>
<span data-ttu-id="7f975-126">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="7f975-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7f975-127">-影像</span><span class="sxs-lookup"><span data-stu-id="7f975-127">-Image</span></span>
<span data-ttu-id="7f975-128">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="7f975-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="7f975-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7f975-129">-ManagedDiskId</span></span>
<span data-ttu-id="7f975-130">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="7f975-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7f975-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="7f975-131">-OsState</span></span>
<span data-ttu-id="7f975-132">指定作業系統狀態。</span><span class="sxs-lookup"><span data-stu-id="7f975-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="7f975-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="7f975-133">-OsType</span></span>
<span data-ttu-id="7f975-134">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="7f975-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="7f975-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="7f975-135">-SnapshotId</span></span>
<span data-ttu-id="7f975-136">指定快照的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f975-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="7f975-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7f975-137">-StorageAccountType</span></span>
<span data-ttu-id="7f975-138">Os 影像磁片的儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="7f975-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="7f975-139">-確認</span><span class="sxs-lookup"><span data-stu-id="7f975-139">-Confirm</span></span>
<span data-ttu-id="7f975-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f975-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f975-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f975-141">-WhatIf</span></span>
<span data-ttu-id="7f975-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f975-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f975-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f975-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f975-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f975-144">CommonParameters</span></span>
<span data-ttu-id="7f975-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f975-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f975-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f975-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f975-147">輸入</span><span class="sxs-lookup"><span data-stu-id="7f975-147">INPUTS</span></span>

### <span data-ttu-id="7f975-148">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7f975-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="7f975-149">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="7f975-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7f975-150">"OperatingSystemStateTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="7f975-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7f975-151">System.object</span><span class="sxs-lookup"><span data-stu-id="7f975-151">System.String</span></span>

### <span data-ttu-id="7f975-152">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="7f975-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7f975-153">System.object</span><span class="sxs-lookup"><span data-stu-id="7f975-153">System.Int32</span></span>

## <span data-ttu-id="7f975-154">輸出</span><span class="sxs-lookup"><span data-stu-id="7f975-154">OUTPUTS</span></span>

### <span data-ttu-id="7f975-155">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7f975-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7f975-156">筆記</span><span class="sxs-lookup"><span data-stu-id="7f975-156">NOTES</span></span>

## <span data-ttu-id="7f975-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f975-157">RELATED LINKS</span></span>
