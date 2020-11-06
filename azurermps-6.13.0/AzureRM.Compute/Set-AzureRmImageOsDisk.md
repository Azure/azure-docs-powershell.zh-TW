---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 74dbe48c40dfa08df9fd224f43774095d10a539c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456124"
---
# <span data-ttu-id="3cc42-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="3cc42-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="3cc42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cc42-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc42-103">在 image 物件上設定作業系統的磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc42-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cc42-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cc42-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc42-105">說明</span><span class="sxs-lookup"><span data-stu-id="3cc42-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc42-106">**AzureRmImageOsDisk** Cmdlet 會在 image 物件上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc42-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="3cc42-107">示例</span><span class="sxs-lookup"><span data-stu-id="3cc42-107">EXAMPLES</span></span>

### <span data-ttu-id="3cc42-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3cc42-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="3cc42-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="3cc42-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="3cc42-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="3cc42-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="3cc42-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="3cc42-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="3cc42-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="3cc42-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3cc42-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="3cc42-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="3cc42-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="3cc42-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3cc42-115">參數</span><span class="sxs-lookup"><span data-stu-id="3cc42-115">PARAMETERS</span></span>

### <span data-ttu-id="3cc42-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="3cc42-116">-BlobUri</span></span>
<span data-ttu-id="3cc42-117">指定 blob 的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3cc42-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="3cc42-118">-快取</span><span class="sxs-lookup"><span data-stu-id="3cc42-118">-Caching</span></span>
<span data-ttu-id="3cc42-119">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="3cc42-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="3cc42-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc42-120">-DefaultProfile</span></span>
<span data-ttu-id="3cc42-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cc42-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc42-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3cc42-122">-DiskSizeGB</span></span>
<span data-ttu-id="3cc42-123">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="3cc42-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3cc42-124">-影像</span><span class="sxs-lookup"><span data-stu-id="3cc42-124">-Image</span></span>
<span data-ttu-id="3cc42-125">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="3cc42-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="3cc42-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="3cc42-126">-ManagedDiskId</span></span>
<span data-ttu-id="3cc42-127">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="3cc42-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="3cc42-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="3cc42-128">-OsState</span></span>
<span data-ttu-id="3cc42-129">指定作業系統狀態。</span><span class="sxs-lookup"><span data-stu-id="3cc42-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="3cc42-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="3cc42-130">-OsType</span></span>
<span data-ttu-id="3cc42-131">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="3cc42-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3cc42-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="3cc42-132">-SnapshotId</span></span>
<span data-ttu-id="3cc42-133">指定快照的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cc42-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="3cc42-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3cc42-134">-StorageAccountType</span></span>
<span data-ttu-id="3cc42-135">Os 影像磁片的儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="3cc42-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="3cc42-136">-確認</span><span class="sxs-lookup"><span data-stu-id="3cc42-136">-Confirm</span></span>
<span data-ttu-id="3cc42-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3cc42-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc42-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc42-138">-WhatIf</span></span>
<span data-ttu-id="3cc42-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3cc42-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cc42-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cc42-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc42-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc42-141">CommonParameters</span></span>
<span data-ttu-id="3cc42-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cc42-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc42-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3cc42-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc42-144">輸入</span><span class="sxs-lookup"><span data-stu-id="3cc42-144">INPUTS</span></span>

### <span data-ttu-id="3cc42-145">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3cc42-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="3cc42-146">"OperatingSystemTypes" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="3cc42-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3cc42-147">"OperatingSystemStateTypes" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="3cc42-147">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3cc42-148">System.object</span><span class="sxs-lookup"><span data-stu-id="3cc42-148">System.String</span></span>

### <span data-ttu-id="3cc42-149">"CachingTypes" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="3cc42-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3cc42-150">System.object</span><span class="sxs-lookup"><span data-stu-id="3cc42-150">System.Int32</span></span>

## <span data-ttu-id="3cc42-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3cc42-151">OUTPUTS</span></span>

### <span data-ttu-id="3cc42-152">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3cc42-152">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3cc42-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3cc42-153">NOTES</span></span>

## <span data-ttu-id="3cc42-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cc42-154">RELATED LINKS</span></span>
